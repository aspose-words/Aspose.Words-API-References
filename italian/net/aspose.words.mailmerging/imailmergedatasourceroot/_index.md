---
title: Interface IMailMergeDataSourceRoot
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.MailMerging.IMailMergeDataSourceRoot interfaccia. Implementa questa interfaccia per consentire la stampa unione da unorigine dati personalizzata con dati masterdetail.
type: docs
weight: 3600
url: /it/net/aspose.words.mailmerging/imailmergedatasourceroot/
---
## IMailMergeDataSourceRoot interface

Implementa questa interfaccia per consentire la stampa unione da un'origine dati personalizzata con dati master-detail.

```csharp
public interface IMailMergeDataSourceRoot
```

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetDataSource](../../aspose.words.mailmerging/imailmergedatasourceroot/getdatasource/)(string) | Il motore di stampa unione di Aspose.Words richiama questo metodo quando incontra l'inizio di una regione di stampa unione di primo livello. |

### Esempi

Esegue la stampa unione da un'origine dati personalizzata con dati master-dettagli.

```csharp
public void CustomDataSourceRoot()
{
    // Crea un documento con due regioni di stampa unione denominate "Washington" e "Seattle".
    string[] mailMergeRegions = { "Vancouver", "Seattle" };
    Document doc = CreateSourceDocumentWithMailMergeRegions(mailMergeRegions);

    // Crea due origini dati per la stampa unione.
    EmployeeList employeesWashingtonBranch = new EmployeeList();
    employeesWashingtonBranch.Add(new Employee("John Doe", "Sales"));
    employeesWashingtonBranch.Add(new Employee("Jane Doe", "Management"));

    EmployeeList employeesSeattleBranch = new EmployeeList();
    employeesSeattleBranch.Add(new Employee("John Cardholder", "Management"));
    employeesSeattleBranch.Add(new Employee("Joe Bloggs", "Sales"));

    // Registra le nostre origini dati per nome in una radice di origine dati.
    // Se stiamo per utilizzare questa radice dell'origine dati in una stampa unione con le regioni,
    // il nome registrato di ciascuna origine deve corrispondere al nome di una regione di stampa unione esistente nel documento di origine della stampa unione.
    DataSourceRoot sourceRoot = new DataSourceRoot();
    sourceRoot.RegisterSource(mailMergeRegions[0], new EmployeeListMailMergeSource(employeesWashingtonBranch));
    sourceRoot.RegisterSource(mailMergeRegions[1], new EmployeeListMailMergeSource(employeesSeattleBranch));

    // Dal momento che abbiamo regioni di stampa unione consecutive, normalmente dovremmo eseguire due unioni di posta.
    // Tuttavia, un'origine di stampa unione con una radice di dati può riempire più aree
    // se la radice contiene tabelle con nomi/colonne corrispondenti.
    doc.MailMerge.ExecuteWithRegions(sourceRoot);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSourceRoot.docx");
}

/// <summary>
/// Crea un documento che contenga regioni di stampa unione consecutive, con i nomi designati dall'array di input,
/// per una tabella dati dei dipendenti.
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
/// Un esempio di una classe "entità dati" nell'applicazione.
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
/// Un esempio di una raccolta tipizzata che contiene i tuoi oggetti "dati".
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
/// Radice dell'origine dati che può essere passata direttamente in una stampa unione che può registrare e contenere molte origini dati figlio.
/// Queste origini devono implementare tutte IMailMergeDataSource e sono registrate e differenziate da un nome
/// che corrisponde a una regione di stampa unione che leggerà i rispettivi dati.
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
/// Origine dati stampa unione personalizzata.
/// </summary>
private class EmployeeListMailMergeSource : IMailMergeDataSource
{
    public EmployeeListMailMergeSource(EmployeeList employees)
    {
        mEmployees = employees;
        mRecordIndex = -1;
    }

    /// <summary>
    /// Un'implementazione standard per passare a un record successivo in una raccolta.
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
    /// Il nome dell'origine dati. Utilizzato da Aspose.Words solo durante l'esecuzione della stampa unione con aree ripetibili.
    /// </summary>
    public string TableName
    {
        get { return "Employees"; }
    }

    /// <summary>
    /// Aspose.Words chiama questo metodo per ottenere un valore per ogni campo di dati.
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
                // Restituisce "false" al motore di stampa unione di Aspose.Words per indicare
                // che non siamo riusciti a trovare un campo con questo nome.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// Le origini dati figlio sono per la stampa unione nidificata.
    /// </summary>
    public IMailMergeDataSource GetChildDataSource(string tableName)
    {
        throw new System.NotImplementedException();
    }

    private readonly EmployeeList mEmployees;
    private int mRecordIndex;
}
```

### Guarda anche

* spazio dei nomi [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../)


