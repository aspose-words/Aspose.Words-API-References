---
title: MailMerge.ExecuteWithRegions
linktitle: ExecuteWithRegions
articleTitle: ExecuteWithRegions
second_title: Aspose.Words per .NET
description: Semplifica la creazione dei tuoi documenti con il metodo MailMerge ExecuteWithRegions, consentendo unioni di posta efficienti da origini dati e regioni personalizzate.
type: docs
weight: 200
url: /it/net/aspose.words.mailmerging/mailmerge/executewithregions/
---
## ExecuteWithRegions(*[IMailMergeDataSource](../../imailmergedatasource/)*) {#executewithregions}

Esegue una stampa unione da un'origine dati personalizzata con regioni di stampa unione.

```csharp
public void ExecuteWithRegions(IMailMergeDataSource dataSource)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| dataSource | IMailMergeDataSource | Un oggetto che implementa l'interfaccia della fonte dati per la stampa unione personalizzata. |

## Osservazioni

Utilizzare questo metodo per riempire i campi di stampa unione nel documento con valori provenienti da qualsiasi origine dati personalizzata, come un file XML o raccolte di oggetti aziendali. È necessario scrivere una classe personalizzata che implementi il metodo.[`IMailMergeDataSource`](../../imailmergedatasource/) interfaccia.

Puoi utilizzare questo metodo solo quando[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) È`falso`, cioè non è necessaria la compatibilità con le lingue da destra a sinistra (come l'arabo o l'ebraico).

## Esempi

Mostra come utilizzare le aree di stampa unione per eseguire una stampa unione annidata.

```csharp
public void CustomDataSource()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Normalmente, i MERGEFIELD contengono il nome di una colonna di un'origine dati di stampa unione.
    // In alternativa, possiamo usare i prefissi "TableStart:" e "TableEnd:" per iniziare/terminare un'area di stampa unione.
    // Ogni regione apparterrà a una tabella il cui nome corrisponde alla stringa immediatamente successiva ai due punti del prefisso.
    builder.InsertField(" MERGEFIELD TableStart:Customers");

    // Questi MERGEFIELD si trovano all'interno dell'area di stampa unione della tabella "Clienti".
    // Quando eseguiamo la stampa unione, questo campo riceverà dati dalle righe in un'origine dati denominata "Clienti".
    builder.Write("Full name:\t");
    builder.InsertField(" MERGEFIELD FullName ");
    builder.Write("\nAddress:\t");
    builder.InsertField(" MERGEFIELD Address ");
    builder.Write("\nOrders:\n");

    // Crea una seconda area di stampa unione all'interno dell'area esterna per un'origine dati denominata "Ordini".
    // Le voci di dati "Ordini" hanno una relazione molti-a-uno con la sorgente dati "Clienti".
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

    // Per eseguire la stampa unione dalla tua origine dati, dobbiamo inserirla in un oggetto che implementa l'interfaccia IMailMergeDataSource.
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
/// Un esempio di una classe "entità dati" figlia nella tua applicazione.
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
 /// Un'origine dati di unione di posta personalizzata che puoi implementare per consentire Aspose.Words
/// per unire tramite posta i dati degli oggetti Cliente nei documenti Microsoft Word.
/// </summary>
public class CustomerMailMergeDataSource : IMailMergeDataSource
{
    public CustomerMailMergeDataSource(CustomerList customers)
    {
        mCustomers = customers;

        // Quando inizializziamo la sorgente dati, la sua posizione deve essere precedente al primo record.
        mRecordIndex = -1;
    }

    /// <summary>
    /// Il nome dell'origine dati. Utilizzato da Aspose.Words solo quando si esegue la stampa unione con aree ripetibili.
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
            // Ottieni l'origine dati secondaria, il cui nome corrisponde all'area di stampa unione che utilizza le sue colonne.
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

        // Quando inizializziamo la sorgente dati, la sua posizione deve essere precedente al primo record.
        mRecordIndex = -1;
    }

    /// <summary>
    /// Il nome dell'origine dati. Utilizzato da Aspose.Words solo quando si esegue la stampa unione con aree ripetibili.
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
    /// Restituisce null perché non abbiamo elementi figlio per questo tipo di oggetto.
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
* spazio dei nomi [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../../)

---

## ExecuteWithRegions(*[IMailMergeDataSourceRoot](../../imailmergedatasourceroot/)*) {#executewithregions_1}

Esegue una stampa unione da un'origine dati personalizzata con regioni di stampa unione.

```csharp
public void ExecuteWithRegions(IMailMergeDataSourceRoot dataSourceRoot)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| dataSourceRoot | IMailMergeDataSourceRoot | Un oggetto che implementa l'interfaccia radice della fonte dati di stampa unione personalizzata. |

## Osservazioni

Utilizzare questo metodo per riempire i campi di stampa unione nel documento con valori provenienti da qualsiasi origine dati personalizzata, come un file XML o raccolte di oggetti aziendali. È necessario scrivere classi personalizzate che implementino il metodo.[`IMailMergeDataSourceRoot`](../../imailmergedatasourceroot/) E[`IMailMergeDataSource`](../../imailmergedatasource/) interfacce.

Puoi utilizzare questo metodo solo quando[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) È`falso`, cioè non è necessaria la compatibilità con le lingue da destra a sinistra (come l'arabo o l'ebraico).

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

* interface [IMailMergeDataSourceRoot](../../imailmergedatasourceroot/)
* class [MailMerge](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../../)

---

## ExecuteWithRegions(*DataSet*) {#executewithregions_2}

Esegue la stampa unione da un**Insieme di dati** in un documento con aree di unione di stampa.

```csharp
public void ExecuteWithRegions(DataSet dataSet)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| dataSet | DataSet | **Insieme di dati** che contiene i dati da inserire nei campi di stampa unione. |

## Osservazioni

Utilizzare questo metodo per eseguire la stampa unione da una o più tabelle in aree di stampa unione ripetibili nel documento. Le aree di stampa unione all'interno del documento cresceranno dinamicamente per contenere i record nelle tabelle corrispondenti.

Ogni tavolo nel**Insieme di dati** deve avere un nome.

Il documento deve avere aree di unione di stampa definite con nomi che fanno riferimento alle tabelle nel**Insieme di dati**.

Per specificare un'area di stampa unione nel documento è necessario inserire due campi di stampa unione per contrassegnare l'inizio e la fine dell'area di stampa unione.

Tutto il contenuto del documento incluso in un'area di stampa unione verrà ripetuto automaticamente per ogni record nell'**Tabella dati**.

Per contrassegnare l'inizio di un'area di unione di posta, inserire un MERGEFIELD con nome TableStart:MyTable, dove MyTable corrisponde a uno dei nomi di tabella nella**Insieme di dati**.

Per contrassegnare la fine dell'area di stampa unione, inserire un altro MERGEFIELD con nome TableEnd:MyTable.

Per inserire un MERGEFIELD in Word utilizzare il comando Inserisci/Campo e selezionare MergeField, quindi digitare il nome del campo.

IL**TableStart** E**TableEnd** i campi devono trovarsi all'interno della stessa sezione del documento.

Se utilizzato all'interno di una tabella,**TableStart** E**TableEnd** deve trovarsi all'interno della stessa riga della tabella.

Le aree di unione di posta in un documento devono essere ben formate (è sempre necessario che ci sia una coppia di corrispondenti **TableStart** E**TableEnd** unire i campi con lo stesso nome di tabella).

## Esempi

Mostra come eseguire una stampa unione annidata con due aree di unione e due tabelle dati.

```csharp
public void ExecuteWithRegionsNested()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Normalmente, i MERGEFIELD contengono il nome di una colonna di un'origine dati di stampa unione.
    // In alternativa, possiamo usare i prefissi "TableStart:" e "TableEnd:" per iniziare/terminare un'area di stampa unione.
    // Ogni regione apparterrà a una tabella il cui nome corrisponde alla stringa immediatamente successiva ai due punti del prefisso.
    builder.InsertField(" MERGEFIELD TableStart:Customers");

    // Questo MERGEFIELD si trova all'interno dell'area di stampa unione della tabella "Clienti".
    // Quando eseguiamo la stampa unione, questo campo riceverà dati dalle righe in un'origine dati denominata "Clienti".
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

    // Crea una seconda area di stampa unione all'interno dell'area esterna per una tabella denominata "Ordini".
    // La tabella "Ordini" ha una relazione molti-a-uno con la tabella "Clienti" nella colonna "CustomerID".
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD TableStart:Orders");
    builder.InsertField(" MERGEFIELD ItemName");
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD Quantity");

    // Termina la regione interna, quindi termina quella esterna. L'apertura e la chiusura di un'area di stampa unione devono
    // si verificano sulla stessa riga di una tabella.
    builder.InsertField(" MERGEFIELD TableEnd:Orders");
    builder.EndTable();

    builder.InsertField(" MERGEFIELD TableEnd:Customers");

    // Crea un set di dati che contiene le due tabelle con i nomi e le relazioni richiesti.
    // Ogni documento di unione per ogni riga della tabella "Clienti" dell'area di unione esterna eseguirà la propria unione di posta sulla tabella "Ordini".
    // Ogni documento di unione visualizzerà tutte le righe della tabella successiva i cui valori della colonna "CustomerID" corrispondono alla riga corrente della tabella "Clienti".
    DataSet customersAndOrders = CreateDataSet();
    doc.MailMerge.ExecuteWithRegions(customersAndOrders);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsNested.docx");
}

/// <summary>
/// Genera un set di dati con due tabelle di dati denominate "Clienti" e "Ordini", con una relazione uno-a-molti sulla colonna "CustomerID".
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
* spazio dei nomi [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../../)

---

## ExecuteWithRegions(*DataTable*) {#executewithregions_3}

Esegue la stampa unione da un**Tabella dati** nel documento con aree di unione.

```csharp
public void ExecuteWithRegions(DataTable dataTable)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| dataTable | DataTable | Origine dati per l'operazione di stampa unione. La tabella deve avere il suoTableName insieme di proprietà. |

## Osservazioni

Il documento deve avere un'area di stampa unione definita con un nome che corrisponda a TableName.

Se nel documento sono definite altre aree di stampa unione, queste vengono lasciate intatte. Ciò consente di eseguire diverse operazioni di stampa unione.

## Esempi

Mostra come formattare le celle durante una stampa unione.

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
/// Formatta le righe della tabella mentre avviene una stampa unione, alternando due colori nelle righe pari/dispari.
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

        // Questo è vero se ci troviamo nella prima colonna, il che significa che ci siamo spostati su una nuova riga.
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
        // Non fare nulla.
    }

    private DocumentBuilder mBuilder;
    private int mRowIdx;
}

/// <summary>
/// Funzione necessaria per l'autoporting di Visual Basic che restituisce la parità del numero passato.
/// </summary>
private static bool IsOdd(int value)
{
    return (value / 2 * 2).Equals(value);
}

/// <summary>
/// Crea un'origine dati per la stampa unione.
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

Mostra come utilizzare le regioni per eseguire due distinte unioni di posta in un unico documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Se vogliamo eseguire due unioni di posta consecutive su un documento mentre prendiamo dati da due tabelle
// in qualsiasi modo correlati tra loro, possiamo separare le unioni di posta con le regioni.
// Normalmente, i MERGEFIELD contengono il nome di una colonna di un'origine dati di stampa unione.
// In alternativa, possiamo usare i prefissi "TableStart:" e "TableEnd:" per iniziare/terminare un'area di stampa unione.
// Ogni regione apparterrà a una tabella il cui nome corrisponde alla stringa immediatamente successiva ai due punti del prefisso.
// Queste regioni sono separate per i dati non correlati, mentre possono essere annidate per i dati gerarchici.
builder.Writeln("\tCities: ");
builder.InsertField(" MERGEFIELD TableStart:Cities");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Cities");
builder.InsertParagraph();

// Entrambi i MERGEFIELD fanno riferimento allo stesso nome di colonna, ma i valori per ciascuno provengono da tabelle dati diverse.
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

// Dovremo eseguire una stampa unione per tabella. La prima stampa unione popolerà i MERGEFIELD.
// nell'intervallo "Città" lasciando vuoti i campi dell'intervallo "Frutta".
doc.MailMerge.ExecuteWithRegions(tableCities);

// Esegui una seconda unione per la tabella "Frutta", utilizzando una vista dati
// per ordinare le righe in ordine crescente nella colonna "Nome" prima dell'unione.
DataView dv = new DataView(tableFruit);
dv.Sort = "Name ASC";
doc.MailMerge.ExecuteWithRegions(dv);

doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsConcurrent.docx");
```

### Guarda anche

* class [MailMerge](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../../)

---

## ExecuteWithRegions(*DataView*) {#executewithregions_4}

Esegue la stampa unione da un**Visualizzazione dati** nel documento con aree di unione.

```csharp
public void ExecuteWithRegions(DataView dataView)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| dataView | DataView | Origine dati per l'operazione di stampa unione. La tabella di origine del**Visualizzazione dati** deve avere il suo**NomeTabella** insieme di proprietà. |

## Osservazioni

Questo metodo è utile se si recuperano dati in un**Tabella dati** ma allora sarebbe necessario applicare un filtro o un ordinamento prima della stampa unione.

Il documento deve avere un'area di stampa unione definita con un nome che corrisponda a **DataView.Table.TableName**.

Se nel documento sono definite altre aree di stampa unione, queste vengono lasciate intatte. Ciò consente di eseguire diverse operazioni di stampa unione.

## Esempi

Mostra come utilizzare le regioni per eseguire due distinte unioni di posta in un unico documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Se vogliamo eseguire due unioni di posta consecutive su un documento mentre prendiamo dati da due tabelle
// in qualsiasi modo correlati tra loro, possiamo separare le unioni di posta con le regioni.
// Normalmente, i MERGEFIELD contengono il nome di una colonna di un'origine dati di stampa unione.
// In alternativa, possiamo usare i prefissi "TableStart:" e "TableEnd:" per iniziare/terminare un'area di stampa unione.
// Ogni regione apparterrà a una tabella il cui nome corrisponde alla stringa immediatamente successiva ai due punti del prefisso.
// Queste regioni sono separate per i dati non correlati, mentre possono essere annidate per i dati gerarchici.
builder.Writeln("\tCities: ");
builder.InsertField(" MERGEFIELD TableStart:Cities");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Cities");
builder.InsertParagraph();

// Entrambi i MERGEFIELD fanno riferimento allo stesso nome di colonna, ma i valori per ciascuno provengono da tabelle dati diverse.
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

// Dovremo eseguire una stampa unione per tabella. La prima stampa unione popolerà i MERGEFIELD.
// nell'intervallo "Città" lasciando vuoti i campi dell'intervallo "Frutta".
doc.MailMerge.ExecuteWithRegions(tableCities);

// Esegui una seconda unione per la tabella "Frutta", utilizzando una vista dati
// per ordinare le righe in ordine crescente nella colonna "Nome" prima dell'unione.
DataView dv = new DataView(tableFruit);
dv.Sort = "Name ASC";
doc.MailMerge.ExecuteWithRegions(dv);

doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsConcurrent.docx");
```

### Guarda anche

* class [MailMerge](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../../)

---

## ExecuteWithRegions(*IDataReader, string*) {#executewithregions_5}

Esegue la stampa unione da**Lettore di dati IData** nel documento con aree di unione.

```csharp
public void ExecuteWithRegions(IDataReader dataReader, string tableName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| dataReader | IDataReader | Origine dei record di dati per la stampa unione come**Lettore dati OleDb** O**Lettore di dati Sql**. |
| tableName | String | Nome dell'area di stampa unione nel documento da popolare. |

## Osservazioni

Puoi passare**Lettore di dati Sql** O**Lettore dati OleDb** oggetto nel metodo this come parametro perché entrambi sono implementati**Lettore di dati IData** interfaccia.

## Esempi

Mostra come inserire in un report le immagini memorizzate in un campo BLOB del database.

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

        // Aprire il lettore dati, che deve essere in una modalità che legge tutti i record contemporaneamente.
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
        // Non fare nulla.
    }

    /// <summary>
    /// Questa funzione viene chiamata quando una stampa unione incontra un MERGEFIELD nel documento con un tag "Image:" nel nome.
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
* spazio dei nomi [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../../)
