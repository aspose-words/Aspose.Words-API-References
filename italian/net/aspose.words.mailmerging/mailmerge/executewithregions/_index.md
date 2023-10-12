---
title: MailMerge.ExecuteWithRegions
second_title: Aspose.Words per .NET API Reference
description: MailMerge metodo. Esegue una stampa unione da unorigine dati personalizzata con aree di stampa unione.
type: docs
weight: 200
url: /it/net/aspose.words.mailmerging/mailmerge/executewithregions/
---
## ExecuteWithRegions(IMailMergeDataSource) {#executewithregions}

Esegue una stampa unione da un'origine dati personalizzata con aree di stampa unione.

```csharp
public void ExecuteWithRegions(IMailMergeDataSource dataSource)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| dataSource | IMailMergeDataSource | Un oggetto che implementa l'interfaccia dell'origine dati di stampa unione personalizzata. |

### Osservazioni

Utilizzare questo metodo per compilare i campi della stampa unione nel documento con valori provenienti da qualsiasi origine dati personalizzata come un file XML o raccolte di oggetti business. Devi scrivere la tua classe personale che implementi il file[`IMailMergeDataSource`](../../imailmergedatasource/) interfaccia.

Puoi utilizzare questo metodo solo quando[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) È`falso`, cioè non è necessaria la compatibilità con le lingue da destra a sinistra (come arabo o ebraico).

### Esempi

Mostra come utilizzare le aree di stampa unione per eseguire una stampa unione nidificata.

```csharp
public void CustomDataSource()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Normalmente, MERGEFIELD contengono il nome di una colonna di un'origine dati di stampa unione.
    // Invece, possiamo utilizzare i prefissi "TableStart:" e "TableEnd:" per iniziare/terminare un'area di stampa unione.
    // Ogni regione apparterrà a una tabella con un nome che corrisponde alla stringa immediatamente dopo i due punti del prefisso.
    builder.InsertField(" MERGEFIELD TableStart:Customers");

    // Questi MERGEFIELD si trovano all'interno dell'area di stampa unione della tabella "Clienti".
    // Quando eseguiamo la stampa unione, questo campo riceverà i dati dalle righe in un'origine dati denominata "Clienti".
    builder.Write("Full name:\t");
    builder.InsertField(" MERGEFIELD FullName ");
    builder.Write("\nAddress:\t");
    builder.InsertField(" MERGEFIELD Address ");
    builder.Write("\nOrders:\n");

    // Crea una seconda regione di stampa unione all'interno della regione esterna per un'origine dati denominata "Ordini".
    // Le voci di dati "Ordini" hanno una relazione molti-a-uno con l'origine dati "Clienti".
    builder.InsertField(" MERGEFIELD TableStart:Orders");

    builder.Write("\tItem name:\t");
    builder.InsertField(" MERGEFIELD Name ");
    builder.Write("\n\tQuantity:\t");
    builder.InsertField(" MERGEFIELD Quantity ");
    builder.InsertParagraph();

    builder.InsertField(" MERGEFIELD TableEnd:Orders");
    builder.InsertField(" MERGEFIELD TableEnd:Customers");

    // Crea dati correlati con nomi che corrispondono a quelli delle nostre regioni di stampa unione.
    CustomerList customers = new CustomerList();
    customers.Add(new Customer("Thomas Hardy", "120 Hanover Sq., London"));
    customers.Add(new Customer("Paolo Accorti", "Via Monte Bianco 34, Torino"));

    customers[0].Orders.Add(new Order("Rugby World Cup Cap", 2));
    customers[0].Orders.Add(new Order("Rugby World Cup Ball", 1));
    customers[1].Orders.Add(new Order("Rugby World Cup Guide", 1));

    // Per eseguire la stampa unione dall'origine dati, è necessario inserirla in un oggetto che implementi l'interfaccia IMailMergeDataSource.
    CustomerMailMergeDataSource customersDataSource = new CustomerMailMergeDataSource(customers);

    doc.MailMerge.ExecuteWithRegions(customersDataSource);

    doc.Save(ArtifactsDir + "NestedMailMergeCustom.CustomDataSource.docx");
}

/// <summary>
/// Un esempio di classe "entità dati" nella tua applicazione.
/// </summary>
public class Customer
{
    public Customer(string aFullName, string anAddress)
    {
        FullName = aFullName;
        Address = anAddress;
        Orders = new List<Order>();
    }

    public string FullName { get; set; }
    public string Address { get; set; }
    public List<Order> Orders { get; set; }
}

/// <summary>
/// Un esempio di una raccolta tipizzata che contiene i tuoi oggetti "dati".
/// </summary>
public class CustomerList : ArrayList
{
    public new Customer this[int index]
    {
        get { return (Customer) base[index]; }
        set { base[index] = value; }
    }
}

/// <summary>
/// Un esempio di una classe "entità dati" secondaria nella tua applicazione.
/// </summary>
public class Order
{
    public Order(string oName, int oQuantity)
    {
        Name = oName;
        Quantity = oQuantity;
    }

    public string Name { get; set; }
    public int Quantity { get; set; }
}

/// <summary>
 /// Un'origine dati di stampa unione personalizzata implementata per consentire Aspose.Words
/// per inviare tramite posta unione i dati dagli oggetti Cliente ai documenti Microsoft Word.
/// </summary>
public class CustomerMailMergeDataSource : IMailMergeDataSource
{
    public CustomerMailMergeDataSource(CustomerList customers)
    {
        mCustomers = customers;

        // Quando inizializziamo l'origine dati, la sua posizione deve essere prima del primo record.
        mRecordIndex = -1;
    }

    /// <summary>
    /// Il nome dell'origine dati. Utilizzato da Aspose.Words solo durante l'esecuzione della stampa unione con regioni ripetibili.
    /// </summary>
    public string TableName
    {
        get { return "Customers"; }
    }

    /// <summary>
    /// Aspose.Words chiama questo metodo per ottenere un valore per ogni campo dati.
    /// </summary>
    public bool GetValue(string fieldName, out object fieldValue)
    {
        switch (fieldName)
        {
            case "FullName":
                fieldValue = mCustomers[mRecordIndex].FullName;
                return true;
            case "Address":
                fieldValue = mCustomers[mRecordIndex].Address;
                return true;
            case "Order":
                fieldValue = mCustomers[mRecordIndex].Orders;
                return true;
            default:
                // Restituisce "false" al motore di stampa unione Aspose.Words per indicare
                // che non siamo riusciti a trovare un campo con questo nome.
                fieldValue = null;
                return false;
        }
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

    public IMailMergeDataSource GetChildDataSource(string tableName)
    {
        switch (tableName)
        {
            // Ottiene l'origine dati figlio, il cui nome corrisponde all'area di stampa unione che utilizza le relative colonne.
            case "Orders":
                return new OrderMailMergeDataSource(mCustomers[mRecordIndex].Orders);
            default:
                return null;
        }
    }

    private bool IsEof
    {
        get { return (mRecordIndex >= mCustomers.Count); }
    }

    private readonly CustomerList mCustomers;
    private int mRecordIndex;
}

public class OrderMailMergeDataSource : IMailMergeDataSource
{
    public OrderMailMergeDataSource(List<Order> orders)
    {
        mOrders = orders;

        // Quando inizializziamo l'origine dati, la sua posizione deve essere prima del primo record.
        mRecordIndex = -1;
    }

    /// <summary>
    /// Il nome dell'origine dati. Utilizzato da Aspose.Words solo durante l'esecuzione della stampa unione con regioni ripetibili.
    /// </summary>
    public string TableName
    {
        get { return "Orders"; }
    }

    /// <summary>
    /// Aspose.Words chiama questo metodo per ottenere un valore per ogni campo dati.
    /// </summary>
    public bool GetValue(string fieldName, out object fieldValue)
    {
        switch (fieldName)
        {
            case "Name":
                fieldValue = mOrders[mRecordIndex].Name;
                return true;
            case "Quantity":
                fieldValue = mOrders[mRecordIndex].Quantity;
                return true;
            default:
                // Restituisce "false" al motore di stampa unione Aspose.Words per indicare
                // che non siamo riusciti a trovare un campo con questo nome.
                fieldValue = null;
                return false;
        }
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

    /// <summary>
    /// Restituisce null perché non abbiamo elementi figli per questo tipo di oggetto.
    /// </summary>
    public IMailMergeDataSource GetChildDataSource(string tableName)
    {
        return null;
    }

    private bool IsEof
    {
        get { return (mRecordIndex >= mOrders.Count); }
    }

    private readonly List<Order> mOrders;
    private int mRecordIndex;
}
```

### Guarda anche

* interface [IMailMergeDataSource](../../imailmergedatasource/)
* class [MailMerge](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../mailmerge/)
* assemblea [Aspose.Words](../../../)

---

## ExecuteWithRegions(IMailMergeDataSourceRoot) {#executewithregions_1}

Esegue una stampa unione da un'origine dati personalizzata con aree di stampa unione.

```csharp
public void ExecuteWithRegions(IMailMergeDataSourceRoot dataSourceRoot)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| dataSourceRoot | IMailMergeDataSourceRoot | Un oggetto che implementa l'interfaccia root dell'origine dati di stampa unione personalizzata. |

### Osservazioni

Utilizzare questo metodo per compilare i campi della stampa unione nel documento con valori provenienti da qualsiasi origine dati personalizzata come un file XML o raccolte di oggetti business. Devi scrivere le tue classi che implementano il file[`IMailMergeDataSourceRoot`](../../imailmergedatasourceroot/) E[`IMailMergeDataSource`](../../imailmergedatasource/) interfacce.

Puoi utilizzare questo metodo solo quando[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) È`falso`, cioè non è necessaria la compatibilità con le lingue da destra a sinistra (come arabo o ebraico).

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

    // Registra le nostre origini dati per nome in una radice dell'origine dati.
    // Se stiamo per utilizzare questa radice dell'origine dati in una stampa unione con regioni,
    // il nome registrato di ciascuna origine deve corrispondere al nome di un'area di stampa unione esistente nel documento di origine della stampa unione.
    DataSourceRoot sourceRoot = new DataSourceRoot();
    sourceRoot.RegisterSource(mailMergeRegions[0], new EmployeeListMailMergeSource(employeesWashingtonBranch));
    sourceRoot.RegisterSource(mailMergeRegions[1], new EmployeeListMailMergeSource(employeesSeattleBranch));

    // Dato che abbiamo regioni di stampa unione consecutive, normalmente dovremmo eseguire due stampe unione.
    // Tuttavia, un'origine di stampa unione con una radice di dati può riempire più regioni
    // se la radice contiene tabelle con nomi/nomi di colonna corrispondenti.
    doc.MailMerge.ExecuteWithRegions(sourceRoot);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSourceRoot.docx");
}

/// <summary>
/// Crea un documento che contenga regioni di stampa unione consecutive, con nomi designati dall'array di input,
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
/// Radice dell'origine dati che può essere passata direttamente a una stampa unione che può registrare e contenere molte origini dati secondarie.
/// Queste origini devono tutte implementare IMailMergeDataSource e sono registrate e differenziate da un nome
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
/// Origine dati di stampa unione personalizzata.
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
    /// Il nome dell'origine dati. Utilizzato da Aspose.Words solo durante l'esecuzione della stampa unione con regioni ripetibili.
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
    /// Le origini dati secondarie sono per le stampe unione nidificate.
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

* interface [IMailMergeDataSourceRoot](../../imailmergedatasourceroot/)
* class [MailMerge](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../mailmerge/)
* assemblea [Aspose.Words](../../../)

---

## ExecuteWithRegions(DataSet) {#executewithregions_2}

Esegue la stampa unione da a **Set di dati** in un documento con regioni di stampa unione.

```csharp
public void ExecuteWithRegions(DataSet dataSet)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| dataSet | DataSet | **Set di dati** che contiene i dati da inserire nei campi della stampa unione. |

### Osservazioni

Utilizzare questo metodo per eseguire la stampa unione da una o più tabelle in aree ripetibili mail merge nel documento. Le aree di stampa unione all'interno del documento aumenteranno dinamicamente per accogliere i record nelle tabelle corrispondenti.

Ogni tavolo in **Set di dati** deve avere un nome.

Il documento deve avere aree di stampa unione definite con nomi che fanno riferimento a tables nel file **Set di dati**.

Per specificare una regione di stampa unione nel documento è necessario inserire due campi di stampa unione per contrassegnare l'inizio e la fine della regione di stampa unione.

Tutto il contenuto del documento incluso in un'area di stampa unione verrà automaticamente ripetuto per ogni record nel file **Tabella dati**.

Per contrassegnare l'inizio di una regione di stampa unione, inserisci un MERGEFIELD con il nome TableStart:MyTable, dove MyTable corrisponde a uno dei nomi di tabella nella tua **Set di dati**.

Per contrassegnare la fine della regione di stampa unione inserire un altro MERGEFIELD con nome TableEnd:MyTable.

Per inserire un MERGEFIELD in Word utilizzare il comando Inserisci/Campo e selezionare Unisci campo, quindi digitare il nome del campo.

IL **Inizio tabella** E **Fine tabella** i campi devono trovarsi all'interno della stessa sezione del documento.

Se utilizzato all'interno di un tavolo, **Inizio tabella** E **Fine tabella** deve essere all'interno della stessa riga nella tabella.

Le regioni di stampa unione in un documento dovrebbero essere ben formate (è sempre necessario che ci sia una coppia di corrispondenti  **Inizio tabella** E **Fine tabella** unire campi con lo stesso nome di tabella).

### Esempi

Mostra come eseguire una stampa unione nidificata con due aree di unione e due tabelle dati.

```csharp
public void ExecuteWithRegionsNested()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Normalmente, MERGEFIELD contengono il nome di una colonna di un'origine dati di stampa unione.
    // Invece, possiamo utilizzare i prefissi "TableStart:" e "TableEnd:" per iniziare/terminare un'area di stampa unione.
    // Ogni regione apparterrà a una tabella con un nome che corrisponde alla stringa immediatamente dopo i due punti del prefisso.
    builder.InsertField(" MERGEFIELD TableStart:Customers");

    // Questo MERGEFIELD si trova all'interno dell'area di stampa unione della tabella "Clienti".
    // Quando eseguiamo la stampa unione, questo campo riceverà i dati dalle righe in un'origine dati denominata "Clienti".
    builder.Write("Orders for ");
    builder.InsertField(" MERGEFIELD CustomerName");
    builder.Write(":");

    // Crea intestazioni di colonna per una tabella che conterrà valori da una seconda regione interna.
    builder.StartTable();
    builder.InsertCell();
    builder.Write("Item");
    builder.InsertCell();
    builder.Write("Quantity");
    builder.EndRow();

    // Crea una seconda regione di stampa unione all'interno della regione esterna per una tabella denominata "Ordini".
    // La tabella "Ordini" ha una relazione molti-a-uno con la tabella "Clienti" nella colonna "ClienteID".
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD TableStart:Orders");
    builder.InsertField(" MERGEFIELD ItemName");
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD Quantity");

    // Termina la regione interna, quindi termina la regione esterna. L'apertura e la chiusura di una regione di stampa unione devono
    // si verificano sulla stessa riga di una tabella.
    builder.InsertField(" MERGEFIELD TableEnd:Orders");
    builder.EndTable();

    builder.InsertField(" MERGEFIELD TableEnd:Customers");

    // Crea un set di dati che contiene le due tabelle con i nomi e le relazioni richiesti.
    // Ogni documento di unione per ogni riga della tabella "Clienti" dell'area di unione esterna eseguirà la stampa unione sulla tabella "Ordini".
    // Ciascun documento di unione visualizzerà tutte le righe dell'ultima tabella i cui valori della colonna "CustomerID" corrispondono alla riga corrente della tabella "Clienti".
    DataSet customersAndOrders = CreateDataSet();
    doc.MailMerge.ExecuteWithRegions(customersAndOrders);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsNested.docx");
}

/// <summary>
/// Genera un set di dati che dispone di due tabelle dati denominate "Clienti" e "Ordini", con una relazione uno-a-molti nella colonna "CustomerID".
/// </summary>
private static DataSet CreateDataSet()
{
    DataTable tableCustomers = new DataTable("Customers");
    tableCustomers.Columns.Add("CustomerID");
    tableCustomers.Columns.Add("CustomerName");
    tableCustomers.Rows.Add(new object[] { 1, "John Doe" });
    tableCustomers.Rows.Add(new object[] { 2, "Jane Doe" });

    DataTable tableOrders = new DataTable("Orders");
    tableOrders.Columns.Add("CustomerID");
    tableOrders.Columns.Add("ItemName");
    tableOrders.Columns.Add("Quantity");
    tableOrders.Rows.Add(new object[] { 1, "Hawaiian", 2 });
    tableOrders.Rows.Add(new object[] { 2, "Pepperoni", 1 });
    tableOrders.Rows.Add(new object[] { 2, "Chicago", 1 });

    DataSet dataSet = new DataSet();
    dataSet.Tables.Add(tableCustomers);
    dataSet.Tables.Add(tableOrders);
    dataSet.Relations.Add(tableCustomers.Columns["CustomerID"], tableOrders.Columns["CustomerID"]);

    return dataSet;
}
```

### Guarda anche

* class [MailMerge](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../mailmerge/)
* assemblea [Aspose.Words](../../../)

---

## ExecuteWithRegions(DataTable) {#executewithregions_3}

Esegue la stampa unione da a **Tabella dati** nel documento con regioni di stampa unione.

```csharp
public void ExecuteWithRegions(DataTable dataTable)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| dataTable | DataTable | Origine dati per l'operazione di stampa unione. La tabella deve avere il suoTableName insieme di proprietà. |

### Osservazioni

Il documento deve avere una regione di stampa unione definita con un nome corrispondente a TableName.

Se nel documento sono definite altre regioni di stampa unione, queste vengono lasciate intatte. Ciò consente di eseguire diverse operazioni di stampa unione.

### Esempi

Illustra come formattare le celle durante una stampa unione.

```csharp
public void AlternatingRows()
{
    Document doc = new Document(MyDir + "Mail merge destination - Northwind suppliers.docx");

    doc.MailMerge.FieldMergingCallback = new HandleMergeFieldAlternatingRows();

    DataTable dataTable = GetSuppliersDataTable();
    doc.MailMerge.ExecuteWithRegions(dataTable);

    doc.Save(ArtifactsDir + "MailMergeEvent.AlternatingRows.docx");
}

/// <summary>
/// Formatta le righe della tabella durante la stampa unione per alternare due colori sulle righe pari/dispari.
/// </summary>
private class HandleMergeFieldAlternatingRows : IFieldMergingCallback
{
    /// <summary>
    /// Chiamato quando una stampa unione unisce i dati in un MERGEFIELD.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (mBuilder == null)
            mBuilder = new DocumentBuilder(args.Document);

        // Questo è vero perché siamo sulla prima colonna, il che significa che ci siamo spostati su una nuova riga.
        if (args.FieldName == "CompanyName")
        {
            Color rowColor = IsOdd(mRowIdx) ? Color.FromArgb(213, 227, 235) : Color.FromArgb(242, 242, 242);

            for (int colIdx = 0; colIdx < 4; colIdx++)
            {
                mBuilder.MoveToCell(0, mRowIdx, colIdx, 0);
                mBuilder.CellFormat.Shading.BackgroundPatternColor = rowColor;
            }

            mRowIdx++;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // Fare niente.
    }

    private DocumentBuilder mBuilder;
    private int mRowIdx;
}

/// <summary>
/// Funzione necessaria per il porting automatico di Visual Basic che restituisce la parità del numero passato.
/// </summary>
private static bool IsOdd(int value)
{
    return (value / 2 * 2).Equals(value);
}

/// <summary>
/// Crea un'origine dati di stampa unione.
/// </summary>
private static DataTable GetSuppliersDataTable()
{
    DataTable dataTable = new DataTable("Suppliers");
    dataTable.Columns.Add("CompanyName");
    dataTable.Columns.Add("ContactName");
    for (int i = 0; i < 10; i++)
    {
        DataRow datarow = dataTable.NewRow();
        dataTable.Rows.Add(datarow);
        datarow[0] = "Company " + i;
        datarow[1] = "Contact " + i;
    }

    return dataTable;
}
```

Mostra come utilizzare le regioni per eseguire due fusioni di posta separate in un unico documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Se vogliamo eseguire due mail merge consecutive su un documento prendendo i dati da due tabelle
// correlati tra loro in alcun modo, possiamo separare le fusioni della posta con le regioni.
// Normalmente, MERGEFIELD contengono il nome di una colonna di un'origine dati di stampa unione.
// Invece, possiamo utilizzare i prefissi "TableStart:" e "TableEnd:" per iniziare/terminare un'area di stampa unione.
// Ogni regione apparterrà a una tabella con un nome che corrisponde alla stringa immediatamente dopo i due punti del prefisso.
// Queste regioni sono separate per i dati non correlati, mentre possono essere annidate per i dati gerarchici.
builder.Writeln("\tCities: ");
builder.InsertField(" MERGEFIELD TableStart:Cities");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Cities");
builder.InsertParagraph();

// Entrambi i MERGEFIELD fanno riferimento allo stesso nome di colonna, ma i valori per ciascuno proverranno da tabelle dati diverse.
builder.Writeln("\tFruit: ");
builder.InsertField(" MERGEFIELD TableStart:Fruit");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Fruit");

// Crea due tabelle di dati non correlate.
DataTable tableCities = new DataTable("Cities");
tableCities.Columns.Add("Name");
tableCities.Rows.Add(new object[] { "Washington" });
tableCities.Rows.Add(new object[] { "London" });
tableCities.Rows.Add(new object[] { "New York" });

DataTable tableFruit = new DataTable("Fruit");
tableFruit.Columns.Add("Name");
tableFruit.Rows.Add(new object[] { "Cherry" });
tableFruit.Rows.Add(new object[] { "Apple" });
tableFruit.Rows.Add(new object[] { "Watermelon" });
tableFruit.Rows.Add(new object[] { "Banana" });

// Dovremo eseguire una stampa unione per tabella. La prima stampa unione popolerà i MERGEFIELD
// nell'intervallo "Città" lasciando vuoti i campi dell'intervallo "Frutta".
doc.MailMerge.ExecuteWithRegions(tableCities);

// Esegue una seconda unione per la tabella "Frutta", utilizzando una visualizzazione dati
// per ordinare le righe in ordine crescente nella colonna "Nome" prima dell'unione.
DataView dv = new DataView(tableFruit);
dv.Sort = "Name ASC";
doc.MailMerge.ExecuteWithRegions(dv);

doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsConcurrent.docx");
```

### Guarda anche

* class [MailMerge](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../mailmerge/)
* assemblea [Aspose.Words](../../../)

---

## ExecuteWithRegions(DataView) {#executewithregions_4}

Esegue la stampa unione da a **DataView** nel documento con regioni di stampa unione.

```csharp
public void ExecuteWithRegions(DataView dataView)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| dataView | DataView | Origine dati per l'operazione di stampa unione. La tabella di origine del **DataView** deve avere il suo **NomeTabella** insieme di proprietà. |

### Osservazioni

Questo metodo è utile se recuperi i dati in un file **Tabella dati** ma poi è necessario applicare un filtro o ordinare prima della stampa unione.

Il documento deve avere una regione di stampa unione definita con un nome corrispondente a  **DataView.Table.TableName**.

Se nel documento sono definite altre regioni di stampa unione, queste vengono lasciate intatte. Ciò consente di eseguire diverse operazioni di stampa unione.

### Esempi

Mostra come utilizzare le regioni per eseguire due fusioni di posta separate in un unico documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Se vogliamo eseguire due mail merge consecutive su un documento prendendo i dati da due tabelle
// correlati tra loro in alcun modo, possiamo separare le fusioni della posta con le regioni.
// Normalmente, MERGEFIELD contengono il nome di una colonna di un'origine dati di stampa unione.
// Invece, possiamo utilizzare i prefissi "TableStart:" e "TableEnd:" per iniziare/terminare un'area di stampa unione.
// Ogni regione apparterrà a una tabella con un nome che corrisponde alla stringa immediatamente dopo i due punti del prefisso.
// Queste regioni sono separate per i dati non correlati, mentre possono essere annidate per i dati gerarchici.
builder.Writeln("\tCities: ");
builder.InsertField(" MERGEFIELD TableStart:Cities");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Cities");
builder.InsertParagraph();

// Entrambi i MERGEFIELD fanno riferimento allo stesso nome di colonna, ma i valori per ciascuno proverranno da tabelle dati diverse.
builder.Writeln("\tFruit: ");
builder.InsertField(" MERGEFIELD TableStart:Fruit");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Fruit");

// Crea due tabelle di dati non correlate.
DataTable tableCities = new DataTable("Cities");
tableCities.Columns.Add("Name");
tableCities.Rows.Add(new object[] { "Washington" });
tableCities.Rows.Add(new object[] { "London" });
tableCities.Rows.Add(new object[] { "New York" });

DataTable tableFruit = new DataTable("Fruit");
tableFruit.Columns.Add("Name");
tableFruit.Rows.Add(new object[] { "Cherry" });
tableFruit.Rows.Add(new object[] { "Apple" });
tableFruit.Rows.Add(new object[] { "Watermelon" });
tableFruit.Rows.Add(new object[] { "Banana" });

// Dovremo eseguire una stampa unione per tabella. La prima stampa unione popolerà i MERGEFIELD
// nell'intervallo "Città" lasciando vuoti i campi dell'intervallo "Frutta".
doc.MailMerge.ExecuteWithRegions(tableCities);

// Esegue una seconda unione per la tabella "Frutta", utilizzando una visualizzazione dati
// per ordinare le righe in ordine crescente nella colonna "Nome" prima dell'unione.
DataView dv = new DataView(tableFruit);
dv.Sort = "Name ASC";
doc.MailMerge.ExecuteWithRegions(dv);

doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsConcurrent.docx");
```

### Guarda anche

* class [MailMerge](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../mailmerge/)
* assemblea [Aspose.Words](../../../)

---

## ExecuteWithRegions(IDataReader, string) {#executewithregions_5}

Esegue la stampa unione da **IDataReader** nel documento con regioni di stampa unione.

```csharp
public void ExecuteWithRegions(IDataReader dataReader, string tableName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| dataReader | IDataReader | Origine dei record di dati per la stampa unione come **Lettore dati OleDb** O **SQLDataReader**. |
| tableName | String | Nome dell'area di stampa unione nel documento da compilare. |

### Osservazioni

Puoi passare **SQLDataReader** O **Lettore dati OleDb**object nel metodo this come parametro perché entrambi sono implementati **IDataReader** interfaccia.

### Esempi

Mostra come inserire in un report le immagini archiviate in un campo BLOB del database.

```csharp
public void ImageFromBlob()
{
    Document doc = new Document(MyDir + "Mail merge destination - Northwind employees.docx");

    doc.MailMerge.FieldMergingCallback = new HandleMergeImageFieldFromBlob();

    string connString = $"Provider=Microsoft.ACE.OLEDB.12.0;Data Source={DatabaseDir + "Northwind.accdb"};";
    string query = "SELECT FirstName, LastName, Title, Address, City, Region, Country, PhotoBLOB FROM Employees";

    using (OleDbConnection conn = new OleDbConnection(connString))
    {
        conn.Open();

        // Apre il lettore dati, che deve essere in una modalità che legga tutti i record contemporaneamente.
        OleDbCommand cmd = new OleDbCommand(query, conn);
        IDataReader dataReader = cmd.ExecuteReader();

        doc.MailMerge.ExecuteWithRegions(dataReader, "Employees");
    }

    doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromBlob.docx");
}

private class HandleMergeImageFieldFromBlob : IFieldMergingCallback
{
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        // Fare niente.
    }

    /// <summary>
    /// Viene chiamato quando una stampa unione incontra un MERGEFIELD nel documento con un tag "Immagine:" nel suo nome.
    /// </summary>
    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        MemoryStream imageStream = new MemoryStream((byte[])e.FieldValue);
        e.ImageStream = imageStream;
    }
}
```

### Guarda anche

* class [MailMerge](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../mailmerge/)
* assemblea [Aspose.Words](../../../)


