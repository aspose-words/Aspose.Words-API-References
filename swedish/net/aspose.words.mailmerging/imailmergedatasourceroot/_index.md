---
title: Interface IMailMergeDataSourceRoot
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.MailMerging.IMailMergeDataSourceRoot gränssnitt. Implementera detta gränssnitt för att tillåta sammanslagning av epost från en anpassad datakälla med huvuddetaljdata.
type: docs
weight: 3820
url: /sv/net/aspose.words.mailmerging/imailmergedatasourceroot/
---
## IMailMergeDataSourceRoot interface

Implementera detta gränssnitt för att tillåta sammanslagning av e-post från en anpassad datakälla med huvuddetaljdata.

```csharp
public interface IMailMergeDataSourceRoot
```

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetDataSource](../../aspose.words.mailmerging/imailmergedatasourceroot/getdatasource/)(string) | Aspose.Words kopplingsmotor använder den här metoden när den stöter på början av en kopplingsregion på toppnivå. |

### Exempel

Utför sammanslagning från en anpassad datakälla med huvuddetaljdata.

```csharp
public void CustomDataSourceRoot()
{
    // Skapa ett dokument med två kopplingsregioner som heter "Washington" och "Seattle".
    string[] mailMergeRegions = { "Vancouver", "Seattle" };
    Document doc = CreateSourceDocumentWithMailMergeRegions(mailMergeRegions);

    // Skapa två datakällor för kopplingen.
    EmployeeList employeesWashingtonBranch = new EmployeeList();
    employeesWashingtonBranch.Add(new Employee("John Doe", "Sales"));
    employeesWashingtonBranch.Add(new Employee("Jane Doe", "Management"));

    EmployeeList employeesSeattleBranch = new EmployeeList();
    employeesSeattleBranch.Add(new Employee("John Cardholder", "Management"));
    employeesSeattleBranch.Add(new Employee("Joe Bloggs", "Sales"));

    // Registrera våra datakällor efter namn i en datakällas rot.
    // Om vi är på väg att använda denna datakällrot i en e-postsammanfogning med regioner,
    // Varje källas registrerade namn måste matcha namnet på en befintlig kopplingsregion i källdokumentet för kopplingen.
    DataSourceRoot sourceRoot = new DataSourceRoot();
    sourceRoot.RegisterSource(mailMergeRegions[0], new EmployeeListMailMergeSource(employeesWashingtonBranch));
    sourceRoot.RegisterSource(mailMergeRegions[1], new EmployeeListMailMergeSource(employeesSeattleBranch));

    // Eftersom vi har på varandra följande kopplingsregioner skulle vi normalt behöva utföra två kopplingar.
    // En kopplingskälla med en datarot kan dock fylla i flera regioner
    // om roten innehåller tabeller med motsvarande namn/kolumnnamn.
    doc.MailMerge.ExecuteWithRegions(sourceRoot);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSourceRoot.docx");
}

/// <summary>
/// Skapa ett dokument som innehåller på varandra följande kopplingsregioner, med namn som anges av inmatningsmatrisen,
/// för en datatabell över anställda.
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
/// Ett exempel på en "data entity"-klass i din applikation.
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
/// Ett exempel på en maskinskriven samling som innehåller dina "data"-objekt.
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
/// Datakällans rot som kan skickas direkt till en e-postkoppling som kan registrera och innehålla många underordnade datakällor.
/// Dessa källor måste alla implementera IMailMergeDataSource och är registrerade och differentierade med ett namn
/// som motsvarar en kopplingsregion som läser respektive data.
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
/// Anpassad kopplingsdatakälla.
/// </summary>
private class EmployeeListMailMergeSource : IMailMergeDataSource
{
    public EmployeeListMailMergeSource(EmployeeList employees)
    {
        mEmployees = employees;
        mRecordIndex = -1;
    }

    /// <summary>
    /// En standardimplementation för att flytta till nästa post i en samling.
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
    /// Namnet på datakällan. Används endast av Aspose.Words när e-postsammanslagning med repeterbara regioner körs.
    /// </summary>
    public string TableName
    {
        get { return "Employees"; }
    }

    /// <summary>
    /// Aspose.Words anropar denna metod för att få ett värde för varje datafält.
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
                // Returnera "false" till Aspose.Words kopplingsmotor för att beteckna
                // att vi inte kunde hitta ett fält med detta namn.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// Underordnade datakällor är för kapslade sammanslagningar.
    /// </summary>
    public IMailMergeDataSource GetChildDataSource(string tableName)
    {
        throw new System.NotImplementedException();
    }

    private readonly EmployeeList mEmployees;
    private int mRecordIndex;
}
```

### Se även

* namnutrymme [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../)


