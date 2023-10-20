---
title: MailMerge.Execute
linktitle: Execute
articleTitle: Execute
second_title: Aspose.Words für .NET
description: MailMerge Execute methode. Führt einen Seriendruck aus einer benutzerdefinierten Datenquelle durch in C#.
type: docs
weight: 180
url: /de/net/aspose.words.mailmerging/mailmerge/execute/
---
## Execute(*[IMailMergeDataSource](../../imailmergedatasource/)*) {#execute}

Führt einen Seriendruck aus einer benutzerdefinierten Datenquelle durch.

```csharp
public void Execute(IMailMergeDataSource dataSource)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| dataSource | IMailMergeDataSource | Ein Objekt, das die benutzerdefinierte Serienbrief-Datenquellenschnittstelle implementiert. |

## Bemerkungen

Verwenden Sie diese Methode, um Seriendruckfelder im Dokument mit Werten aus einer beliebigen Datenquelle wie einer Liste, einer Hashtabelle oder Objekten zu füllen. Sie müssen Ihre eigene Klasse schreiben, die das implementiert[`IMailMergeDataSource`](../../imailmergedatasource/) Schnittstelle.

Sie können diese Methode nur verwenden, wenn[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) Ist`FALSCH`, Das heißt, Sie benötigen keine Rechts-nach-Links-Sprachkompatibilität (z. B. Arabisch oder Hebräisch).

Diese Methode ignoriert dieRemoveUnusedRegions Möglichkeit.

### Siehe auch

* interface [IMailMergeDataSource](../../imailmergedatasource/)
* class [MailMerge](../)
* namensraum [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../../)

---

## Execute(*string[], object[]*) {#execute_5}

Führt einen Seriendruckvorgang für einen einzelnen Datensatz durch.

```csharp
public void Execute(string[] fieldNames, object[] values)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldNames | String[] | Array von Zusammenführungsfeldnamen. Bei Feldnamen wird die Groß-/Kleinschreibung nicht beachtet. Wenn ein Feldname gefunden wird, der im Dokument nicht gefunden wird, wird er ignoriert. |
| values | Object[] | Array von Werten, die in die Zusammenführungsfelder eingefügt werden sollen. Die Anzahl der Elemente in diesem Array muss mit der Anzahl der Elemente in übereinstimmen*fieldNames*. |

## Bemerkungen

Verwenden Sie diese Methode, um Serienbrieffelder im Dokument mit Werten aus einem Array von Objekten zu füllen.

Bei dieser Methode werden Daten nur für einen Datensatz zusammengeführt. Das Array der Feldnamen und das Array der Werte repräsentieren die Daten eines einzelnen Datensatzes.

Bei dieser Methode werden keine Seriendruckbereiche verwendet.

Diese Methode ignoriert dieRemoveUnusedRegions Möglichkeit.

## Beispiele

Zeigt, wie ein Bild aus einem URI als Serienbriefdaten in ein MERGEFIELD zusammengeführt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// MERGEFIELDs mit „Image:“-Tags erhalten während eines Seriendrucks ein Bild.
// Die Zeichenfolge nach dem Doppelpunkt im Tag „Image:“ entspricht einem Spaltennamen
// in der Datenquelle, deren Zellen URIs von Bilddateien enthalten.
builder.InsertField("MERGEFIELD  Image:logo_FromWeb ");
builder.InsertField("MERGEFIELD  Image:logo_FromFileSystem ");

 // Erstellen Sie eine Datenquelle, die URIs von Bildern enthält, die wir zusammenführen.
// Ein URI kann eine Web-URL sein, die auf ein Bild verweist, oder der Dateiname einer Bilddatei im lokalen Dateisystem.
string[] columns = { "logo_FromWeb", "logo_FromFileSystem" };
object[] URIs = { ImageUrl, ImageDir + "Logo.jpg" };

// Einen Serienbrief für eine Datenquelle mit einer Zeile ausführen.
doc.MailMerge.Execute(columns, URIs);

doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromUrl.docx");
```

Zeigt, wie Sie einen Seriendruck durchführen und das Dokument anschließend im Client-Browser speichern.

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

// Das Dokument an den Client-Browser senden.
Assert.That(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null),
    Throws.TypeOf<ArgumentNullException>()); //Wird ausgelöst, weil HttpResponse im Test null ist.

// Wir müssen diese Antwort manuell schließen, um sicherzustellen, dass wir dem Dokument nach dem Speichern keinen überflüssigen Inhalt hinzufügen.
Assert.That(() => response.End(), Throws.TypeOf<NullReferenceException>());
```

### Siehe auch

* class [MailMerge](../)
* namensraum [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../../)

---

## Execute(*DataTable*) {#execute_2}

Führt einen Serienbrief von einer Datentabelle in das Dokument durch.

```csharp
public void Execute(DataTable table)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| table | DataTable | Tabelle, die Daten enthält, die in Serienbrieffelder eingefügt werden sollen. Bei Feldnamen wird die Groß-/Kleinschreibung nicht beachtet. Wenn ein Feldname gefunden wird, der im Dokument nicht gefunden wird, wird er ignoriert. |

## Bemerkungen

Verwenden Sie diese Methode, um Serienbrieffelder im Dokument mit Werten aus a zu füllen.**Datentabelle**.

Alle Datensätze aus der Tabelle werden in das Dokument eingefügt.

Sie können das NEXT-Feld im Word-Dokument verwenden, um dies zu veranlassen[`MailMerge`](../) Objekt zur Auswahl des nächsten Datensatzes aus dem**Datentabelle** und fahren Sie mit dem Zusammenführen fort. Dies kann beim Erstellen von Dokumenten wie Versandetiketten verwendet werden.

Wann[`MailMerge`](../) Das Objekt erreicht das Ende des Hauptdokuments und es sind noch weitere Zeilen darin**Datentabelle**, kopiert es den gesamten Inhalt des Hauptdokuments und hängt ihn an das Ende des Zieldokuments an, wobei ein Abschnitt -Umbruch als Trennzeichen verwendet wird.

Diese Methode ignoriert dieRemoveUnusedRegions Möglichkeit.

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
    // 1 – Verwenden Sie die gesamte Tabelle für den Serienbrief, um für jede Zeile in der Tabelle ein Ausgabe-Serienbriefdokument zu erstellen:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 – Verwenden Sie eine Zeile der Tabelle, um ein Ausgabe-Serienbriefdokument zu erstellen:
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

Führt einen Serienbrief durch**IDataReader** in das Dokument.

```csharp
public void Execute(IDataReader dataReader)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| dataReader | IDataReader | Datenquelle für den Seriendruckvorgang. |

## Bemerkungen

Du kannst passieren**SqlDataReader** oder**OleDbDataReader** Objekt als Parameter in die Methode this ein, da beide implementiert sind**IDataReader** Schnittstelle.

Beachten Sie, dass diese Methode keine Seriendruckbereiche verwendet und bei mehreren Datensätzen das -Dokument durch Wiederholung des gesamten Dokuments wächst.

Diese Methode ignoriert dieRemoveUnusedRegions Möglichkeit.

## Beispiele

Zeigt, wie ein Serienbrief mit Daten von einem Datenleser ausgeführt wird.

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
    // Erstellen Sie einen SQL-Befehl, der Daten für unseren Serienbrief liefert.
    // Die Namen der Tabellenspalten, die diese SELECT-Anweisung zurückgibt
    // muss den oben platzierten Zusammenführungsfeldern entsprechen.
    OleDbCommand command = new OleDbCommand(query, connection);
    command.CommandText = query;
    try
    {                    
        connection.Open();                 
        using (OleDbDataReader reader = command.ExecuteReader())
        {
            // Nehmen Sie die Daten vom Lesegerät und verwenden Sie sie im Serienbrief.
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

Führt einen Serienbrief von einem aus**Datenansicht** in das Dokument.

```csharp
public void Execute(DataView dataView)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| dataView | DataView | Datenquelle für den Seriendruckvorgang. |

## Bemerkungen

Diese Methode ist nützlich, wenn Sie Daten in a abrufen**Datentabelle** aber dann muss vor dem Seriendruck ein Filter oder eine Sortierung angewendet werden.

Beachten Sie, dass diese Methode keine Seriendruckbereiche verwendet und bei mehreren Datensätzen das -Dokument durch Wiederholung des gesamten Dokuments wächst.

Diese Methode ignoriert dieRemoveUnusedRegions Möglichkeit.

## Beispiele

Zeigt, wie Serienbriefdaten mit einem DataView bearbeitet werden.

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

// Wir können eine Datenansicht verwenden, um die Seriendruckdaten zu ändern, ohne Änderungen an der Datentabelle selbst vorzunehmen.
DataView view = new DataView(table);
view.Sort = "Grade DESC";
view.RowFilter = "Grade >= 50";

// Unsere Datenansicht sortiert die Einträge in absteigender Reihenfolge entlang der Spalte „Note“.
// und filtert Zeilen mit Werten von weniger als 50 in dieser Spalte heraus.
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

Führt einen Serienbrief von einem aus**Datenzeile** in das Dokument.

```csharp
public void Execute(DataRow row)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| row | DataRow | Zeile, die Daten enthält, die in Serienbrieffelder eingefügt werden sollen. Bei Feldnamen wird die Groß-/Kleinschreibung nicht beachtet. Wenn ein Feldname gefunden wird, der im Dokument nicht gefunden wird, wird er ignoriert. |

## Bemerkungen

Verwenden Sie diese Methode, um Serienbrieffelder im Dokument mit Werten aus a zu füllen**Datenzeile**.

Diese Methode ignoriert dieRemoveUnusedRegions Möglichkeit.

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
    // 1 – Verwenden Sie die gesamte Tabelle für den Serienbrief, um für jede Zeile in der Tabelle ein Ausgabe-Serienbriefdokument zu erstellen:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 – Verwenden Sie eine Zeile der Tabelle, um ein Ausgabe-Serienbriefdokument zu erstellen:
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
