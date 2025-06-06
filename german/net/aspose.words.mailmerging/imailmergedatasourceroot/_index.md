---
title: IMailMergeDataSourceRoot Interface
linktitle: IMailMergeDataSourceRoot
articleTitle: IMailMergeDataSourceRoot
second_title: Aspose.Words für .NET
description: Nutzen Sie leistungsstarke Serienbrieffunktionen mit Aspose.Words.MailMerging.IMailMergeDataSourceRoot. Integrieren Sie nahtlos benutzerdefinierte Datenquellen für die Master-Detail-Datenverarbeitung.
type: docs
weight: 4510
url: /de/net/aspose.words.mailmerging/imailmergedatasourceroot/
---
## IMailMergeDataSourceRoot interface

Implementieren Sie diese Schnittstelle, um Serienbriefe aus einer benutzerdefinierten Datenquelle mit Master-Detail-Daten zu ermöglichen.

```csharp
public interface IMailMergeDataSourceRoot
```

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetDataSource](../../aspose.words.mailmerging/imailmergedatasourceroot/getdatasource/)(*string*) | Die Serienbrief-Engine von Aspose.Words ruft diese Methode auf, wenn sie auf den Anfang eines Serienbriefbereichs der obersten Ebene stößt. |

## Beispiele

Führt Serienbriefe aus einer benutzerdefinierten Datenquelle mit Master-Detail-Daten durch.

```csharp
public void CustomDataSourceRoot()
{
    // Erstellen Sie ein Dokument mit zwei Serienbriefbereichen namens „Washington“ und „Seattle“.
    string[] mailMergeRegions = { "Vancouver", "Seattle" };
    Document doc = CreateSourceDocumentWithMailMergeRegions(mailMergeRegions);

    // Erstellen Sie zwei Datenquellen für den Serienbrief.
    EmployeeList employeesWashingtonBranch = new EmployeeList();
    employeesWashingtonBranch.Add(new Employee("John Doe", "Sales"));
    employeesWashingtonBranch.Add(new Employee("Jane Doe", "Management"));

    EmployeeList employeesSeattleBranch = new EmployeeList();
    employeesSeattleBranch.Add(new Employee("John Cardholder", "Management"));
    employeesSeattleBranch.Add(new Employee("Joe Bloggs", "Sales"));

    // Registrieren Sie unsere Datenquellen mit Namen in einem Datenquellenstamm.
    // Wenn wir diese Datenquellenwurzel in einem Serienbrief mit Regionen verwenden möchten,
    // Der registrierte Name jeder Quelle muss mit dem Namen eines vorhandenen Seriendruckbereichs im Seriendruck-Quelldokument übereinstimmen.
    DataSourceRoot sourceRoot = new DataSourceRoot();
    sourceRoot.RegisterSource(mailMergeRegions[0], new EmployeeListMailMergeSource(employeesWashingtonBranch));
    sourceRoot.RegisterSource(mailMergeRegions[1], new EmployeeListMailMergeSource(employeesSeattleBranch));

    // Da wir aufeinanderfolgende Serienbriefbereiche haben, müssten wir normalerweise zwei Serienbriefe durchführen.
    // Eine Serienbriefquelle mit einem Datenstamm kann jedoch mehrere Regionen ausfüllen
    // wenn die Wurzel Tabellen mit entsprechenden Namen/Spaltennamen enthält.
    doc.MailMerge.ExecuteWithRegions(sourceRoot);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSourceRoot.docx");
}

/// <summary>
/// Erstellen Sie ein Dokument, das aufeinanderfolgende Serienbriefbereiche enthält, deren Namen durch das Eingabearray bestimmt werden.
/// für eine Datentabelle mit Mitarbeitern.
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
/// Diese Quellen müssen alle IMailMergeDataSource implementieren und sind durch einen Namen registriert und unterschieden
/// Dies entspricht einem Serienbriefbereich, der die entsprechenden Daten liest.
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
    /// Eine Standardimplementierung zum Wechseln zum nächsten Datensatz in einer Sammlung.
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
    /// Der Name der Datenquelle. Wird von Aspose.Words nur beim Ausführen von Serienbriefen mit wiederholbaren Bereichen verwendet.
    /// </summary>
    public string TableName
    {
        get { return "Employees"; }
    }

    /// <summary>
    /// Aspose.Words ruft diese Methode auf, um für jedes Datenfeld einen Wert zu erhalten.
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
                // Gibt "false" an die Aspose.Words-Serienbrief-Engine zurück, um anzuzeigen,
                // dass wir kein Feld mit diesem Namen finden konnten.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// Untergeordnete Datenquellen dienen für verschachtelte Serienbriefe.
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

* namensraum [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../)
