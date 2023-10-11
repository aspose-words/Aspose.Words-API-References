---
title: MailMerge.Execute
second_title: Aspose.Words per .NET API Reference
description: MailMerge metodo. Esegue una stampa unione da unorigine dati personalizzata.
type: docs
weight: 180
url: /it/net/aspose.words.mailmerging/mailmerge/execute/
---
## Execute(IMailMergeDataSource) {#execute}

Esegue una stampa unione da un'origine dati personalizzata.

```csharp
public void Execute(IMailMergeDataSource dataSource)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| dataSource | IMailMergeDataSource | Un oggetto che implementa l'interfaccia dell'origine dati di stampa unione personalizzata. |

### Osservazioni

Utilizzare questo metodo per compilare i campi della stampa unione nel documento con valori provenienti da qualsiasi origine dati come un elenco, una tabella hash o oggetti. Devi scrivere la tua classe personale che implementi il file[`IMailMergeDataSource`](../../imailmergedatasource/) interfaccia.

Puoi utilizzare questo metodo solo quando[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) È`falso`, cioè non è necessaria la compatibilità con le lingue da destra a sinistra (come arabo o ebraico).

Questo metodo ignora il fileRemoveUnusedRegions opzione.

### Guarda anche

* interface [IMailMergeDataSource](../../imailmergedatasource/)
* class [MailMerge](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../mailmerge/)
* assemblea [Aspose.Words](../../../)

---

## Execute(string[], object[]) {#execute_5}

Esegue un'operazione di stampa unione per un singolo record.

```csharp
public void Execute(string[] fieldNames, object[] values)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fieldNames | String[] | Matrice di nomi di campi di unione. I nomi dei campi non fanno distinzione tra maiuscole e minuscole. Se viene rilevato un nome di campo che non si trova nel documento, viene ignorato. |
| values | Object[] | Matrice di valori da inserire nei campi di unione. Il numero di elementi in questa matrice deve essere uguale al numero di elementi in*fieldNames*. |

### Osservazioni

Utilizzare questo metodo per compilare i campi della stampa unione nel documento con valori provenienti da un array di oggetti.

Questo metodo unisce i dati per un solo record. L'array di nomi di campo e l'array di valori rappresentano i dati di un singolo record.

Questo metodo non utilizza le aree di stampa unione.

Questo metodo ignora il fileRemoveUnusedRegions opzione.

### Esempi

Mostra come unire un'immagine da un URI come dati di stampa unione in un MERGEFIELD.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// MERGEFIELD con tag "Immagine:" riceveranno un'immagine durante una stampa unione.
// La stringa dopo i due punti nel tag "Image:" corrisponde al nome di una colonna
// nell'origine dati le cui celle contengono URI di file di immagine.
builder.InsertField("MERGEFIELD  Image:logo_FromWeb ");
builder.InsertField("MERGEFIELD  Image:logo_FromFileSystem ");

 // Crea un'origine dati che contenga gli URI delle immagini che uniremo.
// Un URI può essere un URL Web che punta a un'immagine o il nome file del file system locale di un file immagine.
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
Assert.That(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null),
    Throws.TypeOf<ArgumentNullException>()); //Generato perché HttpResponse è nullo nel test.

// Dovremo chiudere manualmente questa risposta per assicurarci di non aggiungere contenuti superflui al documento dopo il salvataggio.
Assert.That(() => response.End(), Throws.TypeOf<NullReferenceException>());
```

### Guarda anche

* class [MailMerge](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../mailmerge/)
* assemblea [Aspose.Words](../../../)

---

## Execute(DataTable) {#execute_2}

Esegue la stampa unione da un DataTable nel documento.

```csharp
public void Execute(DataTable table)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| table | DataTable | Tabella che contiene i dati da inserire nei campi della stampa unione. I nomi dei campi non fanno distinzione tra maiuscole e minuscole. Se viene rilevato un nome di campo che non si trova nel documento, viene ignorato. |

### Osservazioni

Utilizza questo metodo per compilare i campi della stampa unione nel documento con valori da a  **Tabella dati**.

Tutti i record della tabella vengono uniti nel documento.

È possibile utilizzare il campo NEXT nel documento di Word per causare[`MailMerge`](../) oggetto per selezionare il record successivo da **Tabella dati** e continuare l'unione. Può essere utilizzato durante la creazione di documenti come le etichette postali.

Quando[`MailMerge`](../) L'oggetto raggiunge la fine del documento principale e ci sono ancora più righe nel file **Tabella dati**, copia l'intero contenuto di il documento principale e lo aggiunge alla fine del documento di destinazione utilizzando un'interruzione di sezione come separatore.

Questo metodo ignora il fileRemoveUnusedRegions opzione.

### Esempi

Mostra come eseguire una stampa unione con i dati di un DataTable.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Di seguito sono riportati due modi per utilizzare DataTable come origine dati per una stampa unione.
    // 1 - Utilizza l'intera tabella per la stampa unione per creare un documento di stampa unione di output per ogni riga nella tabella:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Utilizza una riga della tabella per creare un documento di stampa unione di output:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Crea un documento di origine per la stampa unione.
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
* spazio dei nomi [Aspose.Words.MailMerging](../../mailmerge/)
* assemblea [Aspose.Words](../../../)

---

## Execute(IDataReader) {#execute_4}

Esegue la stampa unione da **IDataReader** nel documento.

```csharp
public void Execute(IDataReader dataReader)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| dataReader | IDataReader | Origine dati per l'operazione di stampa unione. |

### Osservazioni

Puoi passare **SQLDataReader** O **Lettore dati OleDb** object nel metodo this come parametro perché entrambi sono implementati **IDataReader** interfaccia.

Tieni presente che questo metodo non utilizza aree di stampa unione e per più record il documento aumenterà ripetendo l'intero documento.

Questo metodo ignora il fileRemoveUnusedRegions opzione.

### Esempi

Mostra come eseguire una stampa unione utilizzando i dati di un lettore di dati.

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

// Crea una stringa di connessione che punta al file di database "Northwind".
// nel nostro file system locale, apri una connessione e imposta una query SQL.
string connectionString = @"Provider = Microsoft.ACE.OLEDB.12.0; Data Source=" + DatabaseDir + "Northwind.accdb";
string query =
    @"SELECT Products.ProductName, Suppliers.CompanyName, Products.QuantityPerUnit, Products.UnitPrice
    FROM Products 
    INNER JOIN Suppliers 
    ON Products.SupplierID = Suppliers.SupplierID";

using (OleDbConnection connection = new OleDbConnection(connectionString))
{
    // Crea un comando SQL che genererà i dati per la nostra stampa unione.
    // I nomi delle colonne della tabella che questa istruzione SELECT restituirà
    // dovrà corrispondere ai campi di unione che abbiamo inserito sopra.
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
* spazio dei nomi [Aspose.Words.MailMerging](../../mailmerge/)
* assemblea [Aspose.Words](../../../)

---

## Execute(DataView) {#execute_3}

Esegue la stampa unione da a **DataView** nel documento.

```csharp
public void Execute(DataView dataView)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| dataView | DataView | Origine dati per l'operazione di stampa unione. |

### Osservazioni

Questo metodo è utile se recuperi i dati in un file **Tabella dati** ma poi è necessario applicare un filtro o ordinare prima della stampa unione.

Tieni presente che questo metodo non utilizza aree di stampa unione e per più record il documento aumenterà ripetendo l'intero documento.

Questo metodo ignora il fileRemoveUnusedRegions opzione.

### Esempi

Mostra come modificare i dati della stampa unione con un DataView.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Congratulations ");
builder.InsertField(" MERGEFIELD Name");
builder.Write(" for passing with a grade of ");
builder.InsertField(" MERGEFIELD Grade");

// Crea una tabella di dati da cui la nostra stampa unione trarrà i dati.
DataTable table = new DataTable("ExamResults");
table.Columns.Add("Name");
table.Columns.Add("Grade");
table.Rows.Add(new object[] { "John Doe", "67" });
table.Rows.Add(new object[] { "Jane Doe", "81" });
table.Rows.Add(new object[] { "John Cardholder", "47" });
table.Rows.Add(new object[] { "Joe Bloggs", "75" });

// Possiamo utilizzare una visualizzazione dati per modificare i dati della stampa unione senza apportare modifiche alla tabella dati stessa.
DataView view = new DataView(table);
view.Sort = "Grade DESC";
view.RowFilter = "Grade >= 50";

// La nostra visualizzazione dati ordina le voci in ordine decrescente lungo la colonna "Voto".
// e filtra le righe con valori inferiori a 50 su quella colonna.
// Tre righe su quattro soddisfano questi criteri in modo che il documento di output contenga tre documenti di unione.
doc.MailMerge.Execute(view);

doc.Save(ArtifactsDir + "MailMerge.ExecuteDataView.docx");
```

### Guarda anche

* class [MailMerge](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../mailmerge/)
* assemblea [Aspose.Words](../../../)

---

## Execute(DataRow) {#execute_1}

Esegue la stampa unione da a **DataRow** nel documento.

```csharp
public void Execute(DataRow row)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| row | DataRow | Riga che contiene i dati da inserire nei campi della stampa unione. I nomi dei campi non fanno distinzione tra maiuscole e minuscole. Se viene rilevato un nome di campo che non si trova nel documento, viene ignorato. |

### Osservazioni

Utilizzare questo metodo per compilare i campi della stampa unione nel documento con valori da a **DataRow**.

Questo metodo ignora il fileRemoveUnusedRegions opzione.

### Esempi

Mostra come eseguire una stampa unione con i dati di un DataTable.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Di seguito sono riportati due modi per utilizzare DataTable come origine dati per una stampa unione.
    // 1 - Utilizza l'intera tabella per la stampa unione per creare un documento di stampa unione di output per ogni riga nella tabella:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Utilizza una riga della tabella per creare un documento di stampa unione di output:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Crea un documento di origine per la stampa unione.
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
* spazio dei nomi [Aspose.Words.MailMerging](../../mailmerge/)
* assemblea [Aspose.Words](../../../)


