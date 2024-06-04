---
title: IMailMergeDataSourceRoot Interface
linktitle: IMailMergeDataSourceRoot
articleTitle: IMailMergeDataSourceRoot
second_title: Aspose.Words for .NET
description: Aspose.Words.MailMerging.IMailMergeDataSourceRoot interface. Implement this interface to allow mail merge from a custom data source with masterdetail data in C#.
type: docs
weight: 4050
url: /net/aspose.words.mailmerging/imailmergedatasourceroot/
---
## IMailMergeDataSourceRoot interface

Implement this interface to allow mail merge from a custom data source with master-detail data.

```csharp
public interface IMailMergeDataSourceRoot
```

## Methods

| Name | Description |
| --- | --- |
| [GetDataSource](../../aspose.words.mailmerging/imailmergedatasourceroot/getdatasource/)(*string*) | The Aspose.Words mail merge engine invokes this method when it encounters a beginning of a top-level mail merge region. |

## Examples

Performs mail merge from a custom data source with master-detail data.

```csharp
public void CustomDataSourceRoot()
{
    // Create a document with two mail merge regions named "Washington" and "Seattle".
    string[] mailMergeRegions = { "Vancouver", "Seattle" };
    Document doc = CreateSourceDocumentWithMailMergeRegions(mailMergeRegions);

    // Create two data sources for the mail merge.
    EmployeeList employeesWashingtonBranch = new EmployeeList();
    employeesWashingtonBranch.Add(new Employee("John Doe", "Sales"));
    employeesWashingtonBranch.Add(new Employee("Jane Doe", "Management"));

    EmployeeList employeesSeattleBranch = new EmployeeList();
    employeesSeattleBranch.Add(new Employee("John Cardholder", "Management"));
    employeesSeattleBranch.Add(new Employee("Joe Bloggs", "Sales"));

    // Register our data sources by name in a data source root.
    //  If we are about to use this data source root in a mail merge with regions,
    // each source's registered name must match the name of an existing mail merge region in the mail merge source document.
    DataSourceRoot sourceRoot = new DataSourceRoot();
    sourceRoot.RegisterSource(mailMergeRegions[0], new EmployeeListMailMergeSource(employeesWashingtonBranch));
    sourceRoot.RegisterSource(mailMergeRegions[1], new EmployeeListMailMergeSource(employeesSeattleBranch));

    // Since we have consecutive mail merge regions, we would normally have to perform two mail merges.
    // However, one mail merge source with a data root can fill in multiple regions
    // if the root contains tables with corresponding names/column names.
    doc.MailMerge.ExecuteWithRegions(sourceRoot);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSourceRoot.docx");
}

/// <summary>
/// Create a document that contains consecutive mail merge regions, with names designated by the input array,
/// for a data table of employees.
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
/// An example of a "data entity" class in your application.
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
/// An example of a typed collection that contains your "data" objects.
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
/// Data source root that can be passed directly into a mail merge which can register and contain many child data sources.
/// These sources must all implement IMailMergeDataSource, and are registered and differentiated by a name
/// which corresponds to a mail merge region that will read the respective data.
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
/// Custom mail merge data source.
/// </summary>
private class EmployeeListMailMergeSource : IMailMergeDataSource
{
    public EmployeeListMailMergeSource(EmployeeList employees)
    {
        mEmployees = employees;
        mRecordIndex = -1;
    }

    /// <summary>
    /// A standard implementation for moving to a next record in a collection.
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
    /// The name of the data source. Used by Aspose.Words only when executing mail merge with repeatable regions.
    /// </summary>
    public string TableName
    {
        get { return "Employees"; }
    }

    /// <summary>
    /// Aspose.Words calls this method to get a value for every data field.
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
                // Return "false" to the Aspose.Words mail merge engine to signify
                // that we could not find a field with this name.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// Child data sources are for nested mail merges.
    /// </summary>
    public IMailMergeDataSource GetChildDataSource(string tableName)
    {
        throw new System.NotImplementedException();
    }

    private readonly EmployeeList mEmployees;
    private int mRecordIndex;
}
```

### See Also

* namespace [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* assembly [Aspose.Words](../../)
