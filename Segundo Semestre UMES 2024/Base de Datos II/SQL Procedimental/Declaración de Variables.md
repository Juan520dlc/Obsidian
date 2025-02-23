Una variable local de Transact-SQL es un objeto que contiene un valor individual de datos de un tipo específico. Esta variable puede ir cambiando de valor dentro del ámbito en el que se específico

##### Declaración de Variable
``` SQL
DECLARE @MyCounter INT;
```

#### Asignación de Valor
``` SQL
USE AdventureWorks2022;
GO

DECLARE @MyVariable INT;

SET @MyVariable = 1;
```

### Ámbito de una variable
Una variable siempre tendrá un ámbito de definición, donde podrá ser invocada para su utilización.
Este ámbito de utilización de la variable puede estar limitado por una transacción, un procedimiento almacenado, un disparador, una función SQL o por la sentencia GO.
En el siguiente ejemplo la sentencia SELECT generará un error de sintaxis debido a  que la variable se encuentra declarada en otro ámbito.
``` SQL
USE AdventureWorks2022;
GO

DECLARE @MyVariable INT;

SET @MyVariable = 1;
GO

SELECT BusinessEntityID,
	NationalIDNumber,
	JobTitle
FROM HumanResources.Employee
WHERE BusinessEntityID = @MyVariable;
```

### Estructura de una Transacción
``` SQL
BEGIN { TRAN | TRANSACTION}
``` 

#### Commit Tran
Confirma una transacción ya declarada y conserva los cambios realizados
``` SQL
COMMIT TRANSACTION @TranName;
```

### Rollback Tran
Da marcha atrás a una transacción y revierte los cambios realizados
``` SQL
ROLLBACK TRANSACTION @TransactionName;
```
##### Ejemplo
```SQL
DECLARE @TranName VARCHAR(20);
SELECT @TranName = 'MyTransaction';

BEGIN TRANSACTION @TranName;
USE AdventureWorks2022;
DELETE FROM AdventureWorks2022.HumanResources.JobCandidate
	WHERE JobCandidateID = 13;

COMMIT TRANSACTION @TranName;
GO
```


