---
title: IMailMergeDataSourceRoot.GetDataSource
linktitle: GetDataSource
articleTitle: GetDataSource
second_title: Aspose.Words para .NET
description: ¡Desbloquea la combinación de correspondencia fluida con Aspose.Words! Descubre cómo el método GetDataSource de IMailMergeDataSourceRoot mejora tu proceso de automatización de documentos.
type: docs
weight: 10
url: /es/net/aspose.words.mailmerging/imailmergedatasourceroot/getdatasource/
---
## IMailMergeDataSourceRoot.GetDataSource method

El motor de combinación de correspondencia Aspose.Words invoca este método cuando encuentra el comienzo de una región de combinación de correspondencia de nivel superior.

```csharp
public IMailMergeDataSource GetDataSource(string tableName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| tableName | String | El nombre de la región de combinación de correspondencia, tal como se especifica en el documento de plantilla. No distingue entre mayúsculas y minúsculas. |

### Valor_devuelto

Un objeto de fuente de datos que proporcionará acceso a los registros de datos de la tabla especificada.

## Observaciones

Cuando el motor de combinación de correspondencia Aspose.Words rellena un documento con datos y encuentra MERGEFIELD TableStart:TableName, , invoca`GetDataSource` En este objeto. Su implementación debe devolver un nuevo objeto de origen de datos. Aspose.Words usará el origen de datos devuelto para rellenar la región de combinación de correspondencia.

Si no existe una fuente de datos (tabla) con el nombre especificado, su implementación debe devolver`nulo` .

## Ejemplos

Realiza la combinación de correspondencia desde una fuente de datos personalizada con datos maestros y detallados.

```csharp
public void CustomDataSourceRoot()
{
    // Cree un documento con dos regiones de combinación de correspondencia denominadas "Washington" y "Seattle".
    string[] mailMergeRegions = { "Vancouver", "Seattle" };
    Document doc = CreateSourceDocumentWithMailMergeRegions(mailMergeRegions);

    // Cree dos fuentes de datos para la combinación de correspondencia.
    EmployeeList employeesWashingtonBranch = new EmployeeList();
    employeesWashingtonBranch.Add(new Employee("John Doe", "Sales"));
    employeesWashingtonBranch.Add(new Employee("Jane Doe", "Management"));

    EmployeeList employeesSeattleBranch = new EmployeeList();
    employeesSeattleBranch.Add(new Employee("John Cardholder", "Management"));
    employeesSeattleBranch.Add(new Employee("Joe Bloggs", "Sales"));

    // Registra nuestras fuentes de datos por nombre en una raíz de fuente de datos.
    // Si estamos a punto de utilizar esta raíz de fuente de datos en una combinación de correspondencia con regiones,
    // El nombre registrado de cada fuente debe coincidir con el nombre de una región de combinación de correspondencia existente en el documento fuente de combinación de correspondencia.
    DataSourceRoot sourceRoot = new DataSourceRoot();
    sourceRoot.RegisterSource(mailMergeRegions[0], new EmployeeListMailMergeSource(employeesWashingtonBranch));
    sourceRoot.RegisterSource(mailMergeRegions[1], new EmployeeListMailMergeSource(employeesSeattleBranch));

    // Dado que tenemos regiones de combinación de correspondencia consecutivas, normalmente tendríamos que realizar dos combinaciones de correspondencia.
    // Sin embargo, una fuente de combinación de correspondencia con una raíz de datos puede completar varias regiones
    // si la raíz contiene tablas con nombres/nombres de columnas correspondientes.
    doc.MailMerge.ExecuteWithRegions(sourceRoot);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSourceRoot.docx");
}

/// <summary>
/// Cree un documento que contenga regiones de combinación de correspondencia consecutivas, con nombres designados por la matriz de entrada,
/// para una tabla de datos de empleados.
/// </summary>
private static Document CreateSourceDocumentWithMailMergeRegions(string[] regions)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    foreach (string s in regions)
    {
        builder.Writeln("\n" + s + " branch: ");
        builder.InsertField(" MERGEFIELD TableStart:" + s);
        builder.InsertField(" MERGEFIELD FullName");
        builder.Write(", ");
        builder.InsertField(" MERGEFIELD Department");
        builder.InsertField(" MERGEFIELD TableEnd:" + s);
    }

    return doc;
}

/// <summary>
/// Un ejemplo de una clase de "entidad de datos" en su aplicación.
/// </summary>
private class Employee
{
    public Employee(string aFullName, string aDepartment)
    {
        FullName = aFullName;
        Department = aDepartment;
    }

    public string FullName { get; }
    public string Department { get; }
}

/// <summary>
/// Un ejemplo de una colección tipificada que contiene sus objetos "datos".
/// </summary>
private class EmployeeList : ArrayList
{
    public new Employee this[int index]
    {
        get { return (Employee)base[index]; }
        set { base[index] = value; }
    }
}

/// <summary>
/// Raíz de la fuente de datos que se puede pasar directamente a una combinación de correspondencia que puede registrar y contener muchas fuentes de datos secundarias.
/// Todas estas fuentes deben implementar IMailMergeDataSource y están registradas y diferenciadas por un nombre
/// que corresponde a una región de combinación de correspondencia que leerá los datos respectivos.
/// </summary>
private class DataSourceRoot : IMailMergeDataSourceRoot
{
    public IMailMergeDataSource GetDataSource(string tableName)
    {
        EmployeeListMailMergeSource source = mSources[tableName];
        source.Reset();
        return mSources[tableName];
    }

    public void RegisterSource(string sourceName, EmployeeListMailMergeSource source)
    {
        mSources.Add(sourceName, source);
    }

    private readonly Dictionary<string, EmployeeListMailMergeSource> mSources = new Dictionary<string, EmployeeListMailMergeSource>();
}

/// <summary>
/// Fuente de datos de combinación de correspondencia personalizada.
/// </summary>
private class EmployeeListMailMergeSource : IMailMergeDataSource
{
    public EmployeeListMailMergeSource(EmployeeList employees)
    {
        mEmployees = employees;
        mRecordIndex = -1;
    }

    /// <summary>
    /// Una implementación estándar para pasar al siguiente registro en una colección.
    /// </summary>
    public bool MoveNext()
    {
        if (!IsEof)
            mRecordIndex++;

        return !IsEof;
    }

    private bool IsEof
    {
        get { return (mRecordIndex >= mEmployees.Count); }
    }

    public void Reset()
    {
        mRecordIndex = -1;
    }

    /// <summary>
    /// El nombre de la fuente de datos. Aspose.Words lo utiliza solo al ejecutar la combinación de correspondencia con regiones repetibles.
    /// </summary>
    public string TableName
    {
        get { return "Employees"; }
    }

    /// <summary>
    /// Aspose.Words llama a este método para obtener un valor para cada campo de datos.
    /// </summary>
    public bool GetValue(string fieldName, out object fieldValue)
    {
        switch (fieldName)
        {
            case "FullName":
                fieldValue = mEmployees[mRecordIndex].FullName;
                return true;
            case "Department":
                fieldValue = mEmployees[mRecordIndex].Department;
                return true;
            default:
                // Devuelve "falso" al motor de combinación de correspondencia Aspose.Words para indicar
                // que no pudimos encontrar un campo con este nombre.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// Las fuentes de datos secundarias son para combinaciones de correspondencia anidadas.
    /// </summary>
    public IMailMergeDataSource GetChildDataSource(string tableName)
    {
        throw new System.NotImplementedException();
    }

    private readonly EmployeeList mEmployees;
    private int mRecordIndex;
}
```

### Ver también

* interface [IMailMergeDataSource](../../imailmergedatasource/)
* interface [IMailMergeDataSourceRoot](../)
* espacio de nombres [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* asamblea [Aspose.Words](../../../)
