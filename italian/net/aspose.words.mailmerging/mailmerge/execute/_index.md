---
title: MailMerge.Execute
linktitle: Execute
articleTitle: Execute
second_title: Aspose.Words per .NET
description: Semplifica il tuo processo di mailing con il metodo MailMerge Execute, unendo senza sforzo i dati da fonti personalizzate per comunicazioni personalizzate.
type: docs
weight: 180
url: /it/net/aspose.words.mailmerging/mailmerge/execute/
---
## Execute(*[IMailMergeDataSource](../../imailmergedatasource/)*) {#execute}

Esegue una stampa unione da una fonte dati personalizzata.

```csharp
public void Execute(IMailMergeDataSource dataSource)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| dataSource | IMailMergeDataSource | Un oggetto che implementa l'interfaccia della fonte dati per la stampa unione personalizzata. |

## Osservazioni

Utilizzare questo metodo per riempire i campi di stampa unione nel documento con valori provenienti da qualsiasi origine dati, come un elenco, una tabella hash o oggetti. È necessario scrivere una classe personalizzata che implementi il metodo.[`IMailMergeDataSource`](../../imailmergedatasource/) interfaccia.

Puoi utilizzare questo metodo solo quando[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) È`falso`, cioè non è necessaria la compatibilità con le lingue da destra a sinistra (come l'arabo o l'ebraico).

Questo metodo ignora ilRemoveUnusedRegions opzione.

## Esempi

Mostra come eseguire una stampa unione con un'origine dati sotto forma di oggetto personalizzato.

```csharp
public void CustomDataSource()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.InsertField(" MERGEFIELD FullName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    List<Customer> customers = new List<Customer>
    {
        new Customer("Thomas Hardy", "120 Hanover Sq., London"),
        new Customer("Paolo Accorti", "Via Monte Bianco 34, Torino")
    };

     // Per utilizzare un oggetto personalizzato come origine dati, è necessario implementare l'interfaccia IMailMergeDataSource.
    CustomerMailMergeDataSource dataSource = new CustomerMailMergeDataSource(customers);

    doc.MailMerge.Execute(dataSource);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSource.docx");
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
    }

    public string FullName { get; set; }
    public string Address { get; set; }
}

/// <summary>
 /// Un'origine dati di unione di posta personalizzata che puoi implementare per consentire Aspose.Words
/// per unire tramite posta i dati degli oggetti Cliente nei documenti Microsoft Word.
/// </summary>
public class CustomerMailMergeDataSource : IMailMergeDataSource
{
    public CustomerMailMergeDataSource(List<Customer> customers)
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
        get { return "Customer"; }
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
        return null;
    }

    private bool IsEof
    {
        get { return (mRecordIndex >= mCustomers.Count); }
    }

    private readonly List<Customer> mCustomers;
    private int mRecordIndex;
}
```

### Guarda anche

* interface [IMailMergeDataSource](../../imailmergedatasource/)
* class [MailMerge](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../../)

---

## Execute(*string[], object[]*) {#execute_5}

Esegue un'operazione di unione di posta per un singolo record.

```csharp
public void Execute(string[] fieldNames, object[] values)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fieldNames | String[] | Array di nomi di campi unione. I nomi dei campi non fanno distinzione tra maiuscole e minuscole. Se viene rilevato un nome di campo non presente nel documento, viene ignorato. |
| values | Object[] | Array di valori da inserire nei campi di unione. Il numero di elementi in questo array deve essere uguale al numero di elementi in*fieldNames*. |

## Osservazioni

Utilizzare questo metodo per riempire i campi di unione posta nel documento con valori provenienti da un array di oggetti.

Questo metodo unisce i dati di un solo record. L'array dei nomi di campo e l'array dei valori rappresentano i dati di un singolo record.

Questo metodo non utilizza le aree di stampa unione.

Questo metodo ignora ilRemoveUnusedRegions opzione.

## Esempi

Mostra come unire un'immagine da un URI come dati di unione di posta in un MERGEFIELD.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// I MERGEFIELD con tag "Image:" riceveranno un'immagine durante una stampa unione.
// La stringa dopo i due punti nel tag "Immagine:" corrisponde al nome di una colonna
// nella sorgente dati le cui celle contengono gli URI dei file immagine.
builder.InsertField("MERGEFIELD  Image:logo_FromWeb ");
builder.InsertField("MERGEFIELD  Image:logo_FromFileSystem ");

 // Crea un'origine dati che contiene gli URI delle immagini che uniremo.
// Un URI può essere un URL web che punta a un'immagine oppure il nome file del file system locale di un file immagine.
string[] columns = { "logo_FromWeb", "logo_FromFileSystem" };
object[] URIs = { ImageUrl, ImageDir + "Logo.jpg" };

// Esegue una stampa unione su un'origine dati con una riga.
doc.MailMerge.Execute(columns, URIs);

doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromUrl.docx");
```

Mostra come eseguire una stampa unione e quindi salvare il documento nel browser client.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD FullName ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Company ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Address ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD City ");

doc.MailMerge.Execute(new string[] { "FullName", "Company", "Address", "City" },
    new object[] { "James Bond", "MI5 Headquarters", "Milbank", "London" });

// Invia il documento al browser client.
//Generato perché HttpResponse è null nel test.
Assert.Throws<ArgumentNullException>(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null));

// Dovremo chiudere manualmente questa risposta per assicurarci di non aggiungere contenuti superflui al documento dopo il salvataggio.
Assert.Throws<NullReferenceException>(() => response.End());
```

### Guarda anche

* class [MailMerge](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../../)

---

## Execute(*DataTable*) {#execute_2}

Esegue la stampa unione da una tabella dati nel documento.

```csharp
public void Execute(DataTable table)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| table | DataTable | Tabella contenente i dati da inserire nei campi di stampa unione. I nomi dei campi non distinguono tra maiuscole e minuscole. Se viene rilevato un nome di campo non presente nel documento, questo viene ignorato. |

## Osservazioni

Utilizzare questo metodo per riempire i campi di unione di posta nel documento con valori da a **Tabella dati**.

Tutti i record della tabella vengono uniti nel documento.

È possibile utilizzare il campo NEXT nel documento Word per causare[`MailMerge`](../) oggetto per selezionare il record successivo da**Tabella dati** e continuare l'unione. Può essere utilizzato durante la creazione di documenti quali etichette postali.

Quando[`MailMerge`](../) l'oggetto raggiunge la fine del documento principale e ci sono ancora more righe nel**Tabella dati**copia l'intero contenuto del documento principale e lo aggiunge alla fine del documento di destinazione utilizzando un'interruzione section come separatore.

Questo metodo ignora ilRemoveUnusedRegions opzione.

## Esempi

Mostra come eseguire una stampa unione con i dati di una DataTable.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Di seguito sono riportati due modi per utilizzare una DataTable come origine dati per una stampa unione.
    // 1 - Utilizza l'intera tabella per la stampa unione per creare un documento di stampa unione in output per ogni riga della tabella:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Utilizzare una riga della tabella per creare un documento di stampa unione in output:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Crea un documento sorgente per la stampa unione.
/// </summary>
private static Document CreateSourceDocExecuteDataTable()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD CustomerName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    return doc;
}
```

### Guarda anche

* class [MailMerge](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../../)

---

## Execute(*IDataReader*) {#execute_4}

Esegue la stampa unione da**Lettore di dati IData** nel documento.

```csharp
public void Execute(IDataReader dataReader)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| dataReader | IDataReader | Origine dati per l'operazione di stampa unione. |

## Osservazioni

Puoi passare**Lettore di dati Sql** O**Lettore dati OleDb**oggetto nel metodo this come parametro perché entrambi sono implementati**Lettore di dati IData** interfaccia.

Si noti che questo metodo non utilizza aree di unione di posta e, per più record, il documento crescerà ripetendo l'intero documento.

Questo metodo ignora ilRemoveUnusedRegions opzione.

## Esempi

Mostra come eseguire una stampa unione utilizzando i dati provenienti da un lettore di dati.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Product:\t");
builder.InsertField(" MERGEFIELD ProductName");
builder.Write("\nSupplier:\t");
builder.InsertField(" MERGEFIELD CompanyName");
builder.Writeln();
builder.InsertField(" MERGEFIELD QuantityPerUnit");
builder.Write(" for $");
builder.InsertField(" MERGEFIELD UnitPrice");

// Crea una stringa di connessione che punta al file di database "Northwind"
// nel nostro file system locale, apriamo una connessione e impostiamo una query SQL.
string connectionString = @"Provider = Microsoft.ACE.OLEDB.12.0; Data Source=" + DatabaseDir + "Northwind.accdb";
string query =
    @"SELECT Products.ProductName, Suppliers.CompanyName, Products.QuantityPerUnit, Products.UnitPrice
    FROM Products 
    INNER JOIN Suppliers 
    ON Products.SupplierID = Suppliers.SupplierID";

using (OleDbConnection connection = new OleDbConnection(connectionString))
{
    // Crea un comando SQL che recupererà i dati per la nostra stampa unione.
    // I nomi delle colonne della tabella che questa istruzione SELECT restituirà
    // dovrà corrispondere ai campi di unione che abbiamo posizionato sopra.
    OleDbCommand command = new OleDbCommand(query, connection);
    command.CommandText = query;
    try
    {
        connection.Open();
        using (OleDbDataReader reader = command.ExecuteReader())
        {
            // Prendi i dati dal lettore e usali nella stampa unione.
            doc.MailMerge.Execute(reader);
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine(ex.Message);
    }
}

doc.Save(ArtifactsDir + "MailMerge.ExecuteDataReader.docx");
```

### Guarda anche

* class [MailMerge](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../../)

---

## Execute(*DataView*) {#execute_3}

Esegue la stampa unione da un**Visualizzazione dati** nel documento.

```csharp
public void Execute(DataView dataView)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| dataView | DataView | Origine dati per l'operazione di stampa unione. |

## Osservazioni

Questo metodo è utile se si recuperano dati in un**Tabella dati** ma allora sarebbe necessario applicare un filtro o un ordinamento prima della stampa unione.

Si noti che questo metodo non utilizza aree di unione di posta e, per più record, il documento crescerà ripetendo l'intero documento.

Questo metodo ignora ilRemoveUnusedRegions opzione.

## Esempi

Mostra come modificare i dati della stampa unione con un DataView.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Congratulations ");
builder.InsertField(" MERGEFIELD Name");
builder.Write(" for passing with a grade of ");
builder.InsertField(" MERGEFIELD Grade");

// Crea una tabella dati da cui la nostra stampa unione prenderà i dati.
DataTable table = new DataTable("ExamResults");
table.Columns.Add("Name");
table.Columns.Add("Grade");
table.Rows.Add(new object[] { "John Doe", "67" });
table.Rows.Add(new object[] { "Jane Doe", "81" });
table.Rows.Add(new object[] { "John Cardholder", "47" });
table.Rows.Add(new object[] { "Joe Bloggs", "75" });

// Possiamo utilizzare una vista dati per modificare i dati della stampa unione senza apportare modifiche alla tabella dati stessa.
DataView view = new DataView(table);
view.Sort = "Grade DESC";
view.RowFilter = "Grade >= 50";

// La nostra vista dati ordina le voci in ordine decrescente lungo la colonna "Voto"
// e filtra le righe con valori inferiori a 50 in quella colonna.
// Tre delle quattro righe soddisfano tali criteri, pertanto il documento di output conterrà tre documenti di unione.
doc.MailMerge.Execute(view);

doc.Save(ArtifactsDir + "MailMerge.ExecuteDataView.docx");
```

### Guarda anche

* class [MailMerge](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../../)

---

## Execute(*DataRow*) {#execute_1}

Esegue la stampa unione da un**Riga di dati** nel documento.

```csharp
public void Execute(DataRow row)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| row | DataRow | Riga contenente i dati da inserire nei campi di stampa unione. I nomi dei campi non distinguono tra maiuscole e minuscole. Se viene rilevato un nome di campo non presente nel documento, questo viene ignorato. |

## Osservazioni

Utilizzare questo metodo per riempire i campi di unione di posta nel documento con valori da un**Riga di dati**.

Questo metodo ignora ilRemoveUnusedRegions opzione.

## Esempi

Mostra come eseguire una stampa unione con i dati di una DataTable.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Di seguito sono riportati due modi per utilizzare una DataTable come origine dati per una stampa unione.
    // 1 - Utilizza l'intera tabella per la stampa unione per creare un documento di stampa unione in output per ogni riga della tabella:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Utilizzare una riga della tabella per creare un documento di stampa unione in output:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Crea un documento sorgente per la stampa unione.
/// </summary>
private static Document CreateSourceDocExecuteDataTable()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD CustomerName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    return doc;
}
```

### Guarda anche

* class [MailMerge](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../../)
