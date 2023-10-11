---
title: IMailMergeDataSourceRoot.GetDataSource
second_title: Aspose.Words für .NET-API-Referenz
description: IMailMergeDataSourceRoot methode. Die MailMergeEngine von Aspose.Words ruft diese Methode auf wenn sie auf den Anfang eines MailMergeBereichs der obersten Ebene stößt.
type: docs
weight: 10
url: /de/net/aspose.words.mailmerging/imailmergedatasourceroot/getdatasource/
---
## IMailMergeDataSourceRoot.GetDataSource method

Die Mail-Merge-Engine von Aspose.Words ruft diese Methode auf, wenn sie auf den Anfang eines Mail-Merge-Bereichs der obersten Ebene stößt.

```csharp
public IMailMergeDataSource GetDataSource(string tableName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| tableName | String | Der Name des Serienbriefbereichs, wie im Vorlagendokument angegeben. Groß- und Kleinschreibung wird nicht beachtet. |

### Rückgabewert

Ein Datenquellenobjekt, das Zugriff auf die Datensätze der angegebenen Tabelle ermöglicht.

### Bemerkungen

Wenn die Mail-Merge-Engines von Aspose.Words ein Dokument mit Daten füllen und auf MERGEFIELD TableStart:TableName, stoßen, wird es aufgerufen`GetDataSource` zu diesem Objekt. Ihre Implementierung muss ein neues Datenquellenobjekt zurückgeben. Aspose.Words verwendet die zurückgegebene Datenquelle, um den Seriendruckbereich zu füllen.

Wenn eine Datenquelle (Tabelle) mit dem angegebenen Namen nicht vorhanden ist, sollte Ihre Implementierung zurückkehren`Null` .

### Beispiele

Führt einen Serienbrief aus einer benutzerdefinierten Datenquelle mit Master-Detail-Daten durch.

```csharp
public void CustomDataSourceRoot()
{
    // Erstellen Sie ein Dokument mit zwei Serienbriefregionen namens „Washington“ und „Seattle“.
    string[] mailMergeRegions = { "Vancouver", "Seattle" };
    Document doc = CreateSourceDocumentWithMailMergeRegions(mailMergeRegions);

    // Zwei Datenquellen für den Serienbrief erstellen.
    EmployeeList employeesWashingtonBranch = new EmployeeList();
    employeesWashingtonBranch.Add(new Employee("John Doe", "Sales"));
    employeesWashingtonBranch.Add(new Employee("Jane Doe", "Management"));

    EmployeeList employeesSeattleBranch = new EmployeeList();
    employeesSeattleBranch.Add(new Employee("John Cardholder", "Management"));
    employeesSeattleBranch.Add(new Employee("Joe Bloggs", "Sales"));

    // Registrieren Sie unsere Datenquellen namentlich in einem Datenquellenstamm.
    // Wenn wir diesen Datenquellenstamm in einem Serienbrief mit Regionen verwenden möchten,
    // Der registrierte Name jeder Quelle muss mit dem Namen einer vorhandenen Serienbriefregion im Serienbrief-Quelldokument übereinstimmen.
    DataSourceRoot sourceRoot = new DataSourceRoot();
    sourceRoot.RegisterSource(mailMergeRegions[0], new EmployeeListMailMergeSource(employeesWashingtonBranch));
    sourceRoot.RegisterSource(mailMergeRegions[1], new EmployeeListMailMergeSource(employeesSeattleBranch));

    // Da wir aufeinanderfolgende Serienbriefbereiche haben, müssten wir normalerweise zwei Serienbriefe durchführen.
    // Allerdings kann eine Serienbriefquelle mit einem Datenstamm mehrere Regionen ausfüllen
    // wenn die Wurzel Tabellen mit entsprechenden Namen/Spaltennamen enthält.
    doc.MailMerge.ExecuteWithRegions(sourceRoot);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSourceRoot.docx");
}

/// <summary>
/// Erstellen Sie ein Dokument, das aufeinanderfolgende Serienbriefbereiche enthält, deren Namen durch das Eingabearray festgelegt werden.
/// für eine Datentabelle von Mitarbeitern.
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
/// Ein Beispiel für eine „Datenentität“-Klasse in Ihrer Anwendung.
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
/// Ein Beispiel für eine typisierte Sammlung, die Ihre „Daten“-Objekte enthält.
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
/// Datenquellenstamm, der direkt an einen Serienbrief übergeben werden kann, der viele untergeordnete Datenquellen registrieren und enthalten kann.
/// Diese Quellen müssen alle IMailMergeDataSource implementieren und werden durch einen Namen registriert und unterschieden
/// was einem Serienbriefbereich entspricht, der die entsprechenden Daten liest.
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
/// Benutzerdefinierte Serienbrief-Datenquelle.
/// </summary>
private class EmployeeListMailMergeSource : IMailMergeDataSource
{
    public EmployeeListMailMergeSource(EmployeeList employees)
    {
        mEmployees = employees;
        mRecordIndex = -1;
    }

    /// <summary>
    /// Eine Standardimplementierung zum Wechseln zu einem nächsten Datensatz in einer Sammlung.
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
    /// Der Name der Datenquelle. Wird von Aspose.Words nur verwendet, wenn Serienbriefe mit wiederholbaren Bereichen ausgeführt werden.
    /// </summary>
    public string TableName
    {
        get { return "Employees"; }
    }

    /// <summary>
    /// Aspose.Words ruft diese Methode auf, um einen Wert für jedes Datenfeld abzurufen.
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
                // „false“ an die Mail-Merge-Engine von Aspose.Words zurückgeben, um es zu kennzeichnen
                // dass wir kein Feld mit diesem Namen finden konnten.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// Untergeordnete Datenquellen sind für verschachtelte Serienbriefe vorgesehen.
    /// </summary>
    public IMailMergeDataSource GetChildDataSource(string tableName)
    {
        throw new System.NotImplementedException();
    }

    private readonly EmployeeList mEmployees;
    private int mRecordIndex;
}
```

### Siehe auch

* interface [IMailMergeDataSource](../../imailmergedatasource/)
* interface [IMailMergeDataSourceRoot](../)
* namensraum [Aspose.Words.MailMerging](../../imailmergedatasourceroot/)
* Montage [Aspose.Words](../../../)


