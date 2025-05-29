---
title: MailMerge.Execute
linktitle: Execute
articleTitle: Execute
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihren Mailing-Prozess mit der MailMerge Execute-Methode und führen Sie mühelos Daten aus benutzerdefinierten Quellen für eine personalisierte Kommunikation zusammen.
type: docs
weight: 180
url: /de/net/aspose.words.mailmerging/mailmerge/execute/
---
## Execute(*[IMailMergeDataSource](../../imailmergedatasource/)*) {#execute}

Führt einen Serienbrief aus einer benutzerdefinierten Datenquelle aus.

```csharp
public void Execute(IMailMergeDataSource dataSource)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| dataSource | IMailMergeDataSource | Ein Objekt, das die benutzerdefinierte Datenquellenschnittstelle für Serienbriefe implementiert. |

## Bemerkungen

Verwenden Sie diese Methode, um Serienbrieffelder im Dokument mit Werten aus einer beliebigen Datenquelle wie einer Liste, einer Hashtabelle oder einem Objekt zu füllen. Sie müssen eine eigene Klasse schreiben, die die[`IMailMergeDataSource`](../../imailmergedatasource/) Schnittstelle.

Sie können diese Methode nur verwenden, wenn[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) Ist`FALSCH`, das heißt, Sie benötigen keine Rechts-nach-links-Kompatibilität mit Sprachen (wie Arabisch oder Hebräisch).

Diese Methode ignoriert dieRemoveUnusedRegions Option.

## Beispiele

Zeigt, wie ein Serienbrief mit einer Datenquelle in Form eines benutzerdefinierten Objekts ausgeführt wird.

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

        // Um ein benutzerdefiniertes Objekt als Datenquelle zu verwenden, muss es die Schnittstelle IMailMergeDataSource implementieren.
    CustomerMailMergeDataSource dataSource = new CustomerMailMergeDataSource(customers);

    doc.MailMerge.Execute(dataSource);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSource.docx");
}

/// <summary>
/// Ein Beispiel für eine „Datenentität“-Klasse in Ihrer Anwendung.
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
    /// Eine benutzerdefinierte Serienbrief-Datenquelle, die Sie implementieren, um Aspose.Words zu ermöglichen
/// um Daten aus Ihren Kundenobjekten per Serienbrief in Microsoft Word-Dokumente zu übertragen.
/// </summary>
public class CustomerMailMergeDataSource : IMailMergeDataSource
{
    public CustomerMailMergeDataSource(List<Customer> customers)
    {
        mCustomers = customers;

        // Wenn wir die Datenquelle initialisieren, muss ihre Position vor dem ersten Datensatz liegen.
        mRecordIndex = -1;
    }

    /// <summary>
    /// Der Name der Datenquelle. Wird von Aspose.Words nur beim Ausführen von Serienbriefen mit wiederholbaren Bereichen verwendet.
    /// </summary>
    public string TableName
    {
        get { return "Customer"; }
    }

    /// <summary>
    /// Aspose.Words ruft diese Methode auf, um für jedes Datenfeld einen Wert zu erhalten.
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
                // Gibt "false" an die Aspose.Words-Serienbrief-Engine zurück, um anzuzeigen,
                // dass wir kein Feld mit diesem Namen finden konnten.
                fieldValue = null;
                return false;
        }
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

### Siehe auch

* interface [IMailMergeDataSource](../../imailmergedatasource/)
* class [MailMerge](../)
* namensraum [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../../)

---

## Execute(*string[], object[]*) {#execute_5}

Führt einen Serienbriefvorgang für einen einzelnen Datensatz aus.

```csharp
public void Execute(string[] fieldNames, object[] values)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldNames | String[] | Array von Seriendruckfeldnamen. Bei Feldnamen wird die Groß- und Kleinschreibung nicht berücksichtigt. Wird ein Feldname gefunden, der im Dokument nicht gefunden wird, wird er ignoriert. |
| values | Object[] | Array von Werten, die in die Seriendruckfelder eingefügt werden sollen. Die Anzahl der Elemente in diesem Array muss mit der Anzahl der Elemente in übereinstimmen*fieldNames*. |

## Bemerkungen

Verwenden Sie diese Methode, um Seriendruckfelder im Dokument mit Werten aus einem Array von Objekten zu füllen.

Diese Methode führt Daten nur für einen Datensatz zusammen. Das Array der Feldnamen und das Array der Werte stellen die Daten eines einzelnen Datensatzes dar.

Bei dieser Methode werden keine Serienbriefbereiche verwendet.

Diese Methode ignoriert dieRemoveUnusedRegions Option.

## Beispiele

Zeigt, wie ein Bild aus einer URI als Serienbriefdaten in ein MERGEFIELD eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// MERGEFIELDs mit „Image:“-Tags erhalten während eines Serienbriefs ein Bild.
// Die Zeichenfolge nach dem Doppelpunkt im Tag „Image:“ entspricht einem Spaltennamen
// in der Datenquelle, deren Zellen URIs von Bilddateien enthalten.
builder.InsertField("MERGEFIELD  Image:logo_FromWeb ");
builder.InsertField("MERGEFIELD  Image:logo_FromFileSystem ");

    // Erstellen Sie eine Datenquelle, die URIs von Bildern enthält, die wir zusammenführen werden.
// Eine URI kann eine Web-URL sein, die auf ein Bild verweist, oder der Dateiname einer Bilddatei im lokalen Dateisystem.
string[] columns = { "logo_FromWeb", "logo_FromFileSystem" };
object[] URIs = { ImageUrl, ImageDir + "Logo.jpg" };

// Führen Sie einen Serienbrief für eine Datenquelle mit einer Zeile aus.
doc.MailMerge.Execute(columns, URIs);

doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromUrl.docx");
```

Zeigt, wie Sie einen Serienbrief erstellen und das Dokument anschließend im Client-Browser speichern.

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

// Senden Sie das Dokument an den Client-Browser.
//Ausgelöst, weil HttpResponse im Test null ist.
Assert.Throws<ArgumentNullException>(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null));

// Wir müssen diese Antwort manuell schließen, um sicherzustellen, dass wir dem Dokument nach dem Speichern keinen überflüssigen Inhalt hinzufügen.
Assert.Throws<NullReferenceException>(() => response.End());
```

### Siehe auch

* class [MailMerge](../)
* namensraum [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../../)

---

## Execute(*DataTable*) {#execute_2}

Führt einen Serienbrief aus einer DataTable in das Dokument aus.

```csharp
public void Execute(DataTable table)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| table | DataTable | Tabelle, die Daten enthält, die in Serienbrieffelder eingefügt werden sollen. Bei Feldnamen wird die Groß-/Kleinschreibung nicht beachtet. Wenn ein Feldname gefunden wird, der im Dokument nicht gefunden wird, wird er ignoriert. |

## Bemerkungen

Verwenden Sie diese Methode, um Serienbrieffelder im Dokument mit Werten aus a zu füllen.**Datentabelle**.

Alle Datensätze aus der Tabelle werden in das Dokument eingefügt.

Sie können das Feld NEXT im Word-Dokument verwenden, um[`MailMerge`](../) Objekt zum Auswählen des nächsten Datensatzes aus**Datentabelle** und mit dem Zusammenführen fortfahren. Dies kann beim Erstellen von Dokumenten wie Adressetiketten verwendet werden.

Wann[`MailMerge`](../) Objekt erreicht das Ende des Hauptdokuments und es gibt noch mehr Zeilen im**Datentabelle**kopiert es den gesamten Inhalt des Hauptdokuments und hängt ihn mit einem Abschnittsumbruch als Trennzeichen an das Ende des Zieldokuments an.

Diese Methode ignoriert dieRemoveUnusedRegions Option.

## Beispiele

Zeigt, wie ein Serienbrief mit Daten aus einer DataTable ausgeführt wird.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Nachfolgend finden Sie zwei Möglichkeiten, eine DataTable als Datenquelle für einen Serienbrief zu verwenden.
    // 1 - Verwenden Sie die gesamte Tabelle für den Seriendruck, um für jede Zeile in der Tabelle ein Ausgabe-Seriendruckdokument zu erstellen:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Verwenden Sie eine Zeile der Tabelle, um ein Serienbrief-Ausgabedokument zu erstellen:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Erstellt ein Serienbrief-Quelldokument.
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

### Siehe auch

* class [MailMerge](../)
* namensraum [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../../)

---

## Execute(*IDataReader*) {#execute_4}

Führt Serienbriefe aus von**IDataReader** in das Dokument.

```csharp
public void Execute(IDataReader dataReader)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| dataReader | IDataReader | Datenquelle für den Serienbriefvorgang. |

## Bemerkungen

Sie können bestehen**SqlDataReader** oder**OleDbDataReader**Objekt in this Methode als Parameter, weil beide implementiert**IDataReader** Schnittstelle.

Beachten Sie, dass bei dieser Methode keine Serienbriefbereiche verwendet werden und dass bei mehreren Datensätzen das Dokument durch Wiederholung des gesamten Dokuments größer wird.

Diese Methode ignoriert dieRemoveUnusedRegions Option.

## Beispiele

Zeigt, wie ein Serienbrief mit Daten aus einem Datenleser ausgeführt wird.

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

// Erstellen Sie eine Verbindungszeichenfolge, die auf die Datenbankdatei „Northwind“ verweist
// Öffnen Sie in unserem lokalen Dateisystem eine Verbindung und richten Sie eine SQL-Abfrage ein.
string connectionString = @"Provider = Microsoft.ACE.OLEDB.12.0; Data Source=" + DatabaseDir + "Northwind.accdb";
string query =
    @"SELECT Products.ProductName, Suppliers.CompanyName, Products.QuantityPerUnit, Products.UnitPrice
    FROM Products 
    INNER JOIN Suppliers 
    ON Products.SupplierID = Suppliers.SupplierID";

using (OleDbConnection connection = new OleDbConnection(connectionString))
{
    // Erstellen Sie einen SQL-Befehl, der Daten für unseren Serienbrief beschafft.
    // Die Namen der Tabellenspalten, die diese SELECT-Anweisung zurückgibt
    // muss den Seriendruckfeldern entsprechen, die wir oben platziert haben.
    OleDbCommand command = new OleDbCommand(query, connection);
    command.CommandText = query;
    try
    {
        connection.Open();
        using (OleDbDataReader reader = command.ExecuteReader())
        {
            // Daten vom Reader übernehmen und im Serienbrief verwenden.
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

### Siehe auch

* class [MailMerge](../)
* namensraum [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../../)

---

## Execute(*DataView*) {#execute_3}

Führt Serienbriefe aus einem**Datenansicht** in das Dokument.

```csharp
public void Execute(DataView dataView)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| dataView | DataView | Datenquelle für den Serienbriefvorgang. |

## Bemerkungen

Diese Methode ist nützlich, wenn Sie Daten in ein**Datentabelle** aber dann muss vor dem Seriendruck ein Filter oder eine Sortierung angewendet werden.

Beachten Sie, dass bei dieser Methode keine Serienbriefbereiche verwendet werden und dass bei mehreren Datensätzen das Dokument durch Wiederholung des gesamten Dokuments größer wird.

Diese Methode ignoriert dieRemoveUnusedRegions Option.

## Beispiele

Zeigt, wie Serienbriefdaten mit einer DataView bearbeitet werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Congratulations ");
builder.InsertField(" MERGEFIELD Name");
builder.Write(" for passing with a grade of ");
builder.InsertField(" MERGEFIELD Grade");

// Erstellen Sie eine Datentabelle, aus der unser Serienbrief Daten bezieht.
DataTable table = new DataTable("ExamResults");
table.Columns.Add("Name");
table.Columns.Add("Grade");
table.Rows.Add(new object[] { "John Doe", "67" });
table.Rows.Add(new object[] { "Jane Doe", "81" });
table.Rows.Add(new object[] { "John Cardholder", "47" });
table.Rows.Add(new object[] { "Joe Bloggs", "75" });

// Wir können eine Datenansicht verwenden, um die Serienbriefdaten zu ändern, ohne Änderungen an der Datentabelle selbst vorzunehmen.
DataView view = new DataView(table);
view.Sort = "Grade DESC";
view.RowFilter = "Grade >= 50";

// Unsere Datenansicht sortiert die Einträge absteigend entlang der Spalte „Note“
// und filtert Zeilen mit Werten unter 50 in dieser Spalte heraus.
// Drei der vier Zeilen erfüllen diese Kriterien, sodass das Ausgabedokument drei Zusammenführungsdokumente enthält.
doc.MailMerge.Execute(view);

doc.Save(ArtifactsDir + "MailMerge.ExecuteDataView.docx");
```

### Siehe auch

* class [MailMerge](../)
* namensraum [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../../)

---

## Execute(*DataRow*) {#execute_1}

Führt Serienbriefe aus einem**Datenzeile** in das Dokument.

```csharp
public void Execute(DataRow row)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| row | DataRow | Zeile, die Daten enthält, die in Serienbrieffelder eingefügt werden sollen. Bei Feldnamen wird die Groß-/Kleinschreibung nicht beachtet. Wenn ein Feldname gefunden wird, der im Dokument nicht gefunden wird, wird er ignoriert. |

## Bemerkungen

Mit dieser Methode füllen Sie Serienbrieffelder im Dokument mit Werten aus einem**Datenzeile**.

Diese Methode ignoriert dieRemoveUnusedRegions Option.

## Beispiele

Zeigt, wie ein Serienbrief mit Daten aus einer DataTable ausgeführt wird.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Nachfolgend finden Sie zwei Möglichkeiten, eine DataTable als Datenquelle für einen Serienbrief zu verwenden.
    // 1 - Verwenden Sie die gesamte Tabelle für den Seriendruck, um für jede Zeile in der Tabelle ein Ausgabe-Seriendruckdokument zu erstellen:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Verwenden Sie eine Zeile der Tabelle, um ein Serienbrief-Ausgabedokument zu erstellen:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Erstellt ein Serienbrief-Quelldokument.
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

### Siehe auch

* class [MailMerge](../)
* namensraum [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../../)
