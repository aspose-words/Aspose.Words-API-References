---
title: IMailMergeDataSourceRoot.GetDataSource
linktitle: GetDataSource
articleTitle: GetDataSource
second_title: Aspose.Words per .NET
description: Sblocca l'unione di email senza interruzioni con Aspose.Words! Scopri come il metodo GetDataSource di IMailMergeDataSourceRoot migliora il processo di automazione dei documenti.
type: docs
weight: 10
url: /it/net/aspose.words.mailmerging/imailmergedatasourceroot/getdatasource/
---
## IMailMergeDataSourceRoot.GetDataSource method

Il motore di stampa unione Aspose.Words richiama questo metodo quando incontra l'inizio di un'area di stampa unione di livello superiore.

```csharp
public IMailMergeDataSource GetDataSource(string tableName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| tableName | String | Nome dell'area di stampa unione come specificato nel documento modello. Non distingue tra maiuscole e minuscole. |

### Valore di ritorno

Un oggetto sorgente dati che fornirà l'accesso ai record di dati della tabella specificata.

## Osservazioni

Quando i motori di stampa unione Aspose.Words popolano un documento con dati e incontrano MERGEFIELD TableStart:TableName, richiama`GetDataSource` Su questo oggetto. L'implementazione deve restituire un nuovo oggetto sorgente dati. Aspose.Words utilizzerà la sorgente dati restituita per popolare l'area di stampa unione.

Se un'origine dati (tabella) con il nome specificato non esiste, l'implementazione dovrebbe restituire`null` .

## Esempi

Esegue la stampa unione da un'origine dati personalizzata con dati master-detail.

```csharp
public void CustomDataSourceRoot()
{
    // Crea un documento con due aree di stampa unione denominate "Washington" e "Seattle".
    string[] mailMergeRegions = { "Vancouver", "Seattle" };
    Document doc = CreateSourceDocumentWithMailMergeRegions(mailMergeRegions);

    // Crea due origini dati per la stampa unione.
    EmployeeList employeesWashingtonBranch = new EmployeeList();
    employeesWashingtonBranch.Add(new Employee("John Doe", "Sales"));
    employeesWashingtonBranch.Add(new Employee("Jane Doe", "Management"));

    EmployeeList employeesSeattleBranch = new EmployeeList();
    employeesSeattleBranch.Add(new Employee("John Cardholder", "Management"));
    employeesSeattleBranch.Add(new Employee("Joe Bloggs", "Sales"));

    // Registra le nostre fonti dati in base al nome in una radice della fonte dati.
    // Se stiamo per utilizzare questa radice di origine dati in una stampa unione con regioni,
    // il nome registrato di ogni origine deve corrispondere al nome di un'area di stampa unione esistente nel documento di origine della stampa unione.
    DataSourceRoot sourceRoot = new DataSourceRoot();
    sourceRoot.RegisterSource(mailMergeRegions[0], new EmployeeListMailMergeSource(employeesWashingtonBranch));
    sourceRoot.RegisterSource(mailMergeRegions[1], new EmployeeListMailMergeSource(employeesSeattleBranch));

    // Poiché abbiamo aree di stampa unione consecutive, normalmente dovremmo eseguire due stampe unione.
    // Tuttavia, un'origine di stampa unione con una radice dati può riempire più regioni
    // se la radice contiene tabelle con nomi/nomi di colonna corrispondenti.
    doc.MailMerge.ExecuteWithRegions(sourceRoot);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSourceRoot.docx");
}

/// <summary>
/// Crea un documento che contiene aree di unione di stampa consecutive, con nomi designati dalla matrice di input,
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
/// Un esempio di classe "entità dati" nella tua applicazione.
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
/// Radice della fonte dati che può essere passata direttamente in una stampa unione che può registrare e contenere molte fonti dati secondarie.
/// Tutte queste fonti devono implementare IMailMergeDataSource e sono registrate e differenziate da un nome
/// che corrisponde a un'area di stampa unione che leggerà i rispettivi dati.
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
/// Origine dati per la stampa unione personalizzata.
/// </summary>
private class EmployeeListMailMergeSource : IMailMergeDataSource
{
    public EmployeeListMailMergeSource(EmployeeList employees)
    {
        mEmployees = employees;
        mRecordIndex = -1;
    }

    /// <summary>
    /// Un'implementazione standard per passare al record successivo in una raccolta.
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
    /// Il nome dell'origine dati. Utilizzato da Aspose.Words solo quando si esegue la stampa unione con aree ripetibili.
    /// </summary>
    public string TableName
    {
        get { return "Employees"; }
    }

    /// <summary>
    /// Aspose.Words chiama questo metodo per ottenere un valore per ogni campo dati.
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
                // Restituisce "false" al motore di stampa unione Aspose.Words per indicare
                // che non siamo riusciti a trovare un campo con questo nome.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// Le origini dati figlio sono per le unioni di posta nidificate.
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

* interface [IMailMergeDataSource](../../imailmergedatasource/)
* interface [IMailMergeDataSourceRoot](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../../)
