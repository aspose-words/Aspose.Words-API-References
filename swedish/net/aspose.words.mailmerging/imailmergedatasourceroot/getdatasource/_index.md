---
title: IMailMergeDataSourceRoot.GetDataSource
linktitle: GetDataSource
articleTitle: GetDataSource
second_title: Aspose.Words för .NET
description: Få sömlös dokumentkoppling med Aspose.Words! Upptäck hur metoden IMailMergeDataSourceRoot GetDataSource förbättrar din dokumentautomatiseringsprocess.
type: docs
weight: 10
url: /sv/net/aspose.words.mailmerging/imailmergedatasourceroot/getdatasource/
---
## IMailMergeDataSourceRoot.GetDataSource method

Aspose.Words-kopplingsmotorn anropar den här metoden när den stöter på början av en region för koppling av dokument på toppnivå.

```csharp
public IMailMergeDataSource GetDataSource(string tableName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| tableName | String | Namnet på den kopplade dokumentregionen som anges i malldokumentet. Skiftlägesokänsligt. |

### Returvärde

Ett datakällobjekt som ger åtkomst till dataposterna i den angivna tabellen.

## Anmärkningar

När Aspose.Words-kopplingsmotorerna fyller ett dokument med data och stöter på MERGEFIELD TableStart:TableName, som den anropar`GetDataSource` på det här objektet. Din implementering behöver returnera ett nytt datakällobjekt. Aspose.Words kommer att använda den returnerade datakällan för att fylla i kopplingsområdet.

Om en datakälla (tabell) med det angivna namnet inte finns, ska din implementering returnera`null` .

## Exempel

Utför dokumentkoppling från en anpassad datakälla med huvud-/detaljdata.

```csharp
public void CustomDataSourceRoot()
{
    // Skapa ett dokument med två kopplingsområden med namnet "Washington" och "Seattle".
    string[] mailMergeRegions = { "Vancouver", "Seattle" };
    Document doc = CreateSourceDocumentWithMailMergeRegions(mailMergeRegions);

    // Skapa två datakällor för dokumentkopplingen.
    EmployeeList employeesWashingtonBranch = new EmployeeList();
    employeesWashingtonBranch.Add(new Employee("John Doe", "Sales"));
    employeesWashingtonBranch.Add(new Employee("Jane Doe", "Management"));

    EmployeeList employeesSeattleBranch = new EmployeeList();
    employeesSeattleBranch.Add(new Employee("John Cardholder", "Management"));
    employeesSeattleBranch.Add(new Employee("Joe Bloggs", "Sales"));

    // Registrera våra datakällor med namn i en datakällrot.
    // Om vi ska använda den här datakällans rot i en dokumentkoppling med regioner,
    // varje källas registrerade namn måste matcha namnet på en befintlig region för dokumentkoppling i källdokumentet för dokumentkopplingen.
    DataSourceRoot sourceRoot = new DataSourceRoot();
    sourceRoot.RegisterSource(mailMergeRegions[0], new EmployeeListMailMergeSource(employeesWashingtonBranch));
    sourceRoot.RegisterSource(mailMergeRegions[1], new EmployeeListMailMergeSource(employeesSeattleBranch));

    // Eftersom vi har områden för dokumentkopplingar som följer efter varandra, skulle vi normalt behöva utföra två dokumentkopplingar.
    // En enda källa för koppling av dokument med en datarot kan dock fylla i flera regioner
    // om roten innehåller tabeller med motsvarande namn/kolumnnamn.
    doc.MailMerge.ExecuteWithRegions(sourceRoot);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSourceRoot.docx");
}

/// <summary>
/// Skapa ett dokument som innehåller efterföljande dokumentkopplingsområden, med namn som anges av inmatningsmatrisen,
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
/// Ett exempel på en typad samling som innehåller dina "data"-objekt.
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
/// Datakällans rot som kan skickas direkt till en dokumentkoppling som kan registrera och innehålla många underordnade datakällor.
/// Dessa källor måste alla implementera IMailMergeDataSource och vara registrerade och differentierade med ett namn
/// vilket motsvarar ett område för dokumentkoppling som läser respektive data.
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
/// Anpassad datakälla för dokumentkoppling.
/// </summary>
private class EmployeeListMailMergeSource : IMailMergeDataSource
{
    public EmployeeListMailMergeSource(EmployeeList employees)
    {
        mEmployees = employees;
        mRecordIndex = -1;
    }

    /// <summary>
    /// En standardimplementering för att gå till nästa post i en samling.
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
    /// Namnet på datakällan. Används endast av Aspose.Words vid dokumentkoppling med repeterbara regioner.
    /// </summary>
    public string TableName
    {
        get { return "Employees"; }
    }

    /// <summary>
    /// Aspose.Words anropar den här metoden för att hämta ett värde för varje datafält.
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
                // Returnera "false" till Aspose.Words-kopplingsmotorn för att beteckna
                // att vi inte kunde hitta ett fält med detta namn.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// Underordnade datakällor är för kapslade dokumentkopplingar.
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

* interface [IMailMergeDataSource](../../imailmergedatasource/)
* interface [IMailMergeDataSourceRoot](../)
* namnutrymme [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../../)
