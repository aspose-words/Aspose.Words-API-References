---
title: Execute
second_title: Aspose.Words für .NET-API-Referenz
description: Führt einen Seriendruck aus einer benutzerdefinierten Datenquelle durch.
type: docs
weight: 180
url: /de/net/aspose.words.mailmerging/mailmerge/execute/
---
## Execute(IMailMergeDataSource) {#execute}

Führt einen Seriendruck aus einer benutzerdefinierten Datenquelle durch.

```csharp
public void Execute(IMailMergeDataSource dataSource)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| dataSource | IMailMergeDataSource | Ein Objekt, das die benutzerdefinierte Seriendruck-Datenquellenschnittstelle implementiert. |

### Bemerkungen

Verwenden Sie diese Methode, um Serienbrieffelder im Dokument mit Werten aus einer beliebigen Datenquelle wie einer Liste oder Hashtabelle oder Objekten zu füllen. Sie müssen Ihre eigene Klasse schreiben, die die implementiert[`IMailMergeDataSource`](../../imailmergedatasource) Schnittstelle.

Sie können diese Methode nur verwenden, wenn[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate)ist false, , das heißt, Sie benötigen keine Rechts-nach-links-Sprachkompatibilität (wie Arabisch oder Hebräisch).

Diese Methode ignoriert dieRemoveUnusedRegions Möglichkeit.

### Siehe auch

* interface [IMailMergeDataSource](../../imailmergedatasource)
* class [MailMerge](../../mailmerge)
* namensraum [Aspose.Words.MailMerging](../../mailmerge)
* Montage [Aspose.Words](../../../)

---

## Execute(string[], object[]) {#execute_5}

Führt einen Seriendruckvorgang für einen einzelnen Datensatz durch.

```csharp
public void Execute(string[] fieldNames, object[] values)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldNames | String[] | Array von Briefvorlagenfeldnamen. Bei Feldnamen wird nicht zwischen Groß- und Kleinschreibung unterschieden. Wenn ein Feldname gefunden wird, der nicht im Dokument gefunden wird, wird er ignoriert. |
| values | Object[] | Array von Werten, die in die Briefvorlagenfelder eingefügt werden sollen. Die Anzahl der Elemente in diesem Array muss mit der Anzahl der Elemente in fieldNames übereinstimmen. |

### Bemerkungen

Verwenden Sie diese Methode, um Serienbrieffelder im Dokument mit Werten aus einem Array von Objekten zu füllen.

Bei dieser Methode werden Daten nur für einen Datensatz zusammengeführt. Das Array von Feldnamen und das Array von Werten repräsentieren die Daten eines einzelnen Datensatzes.

Diese Methode verwendet keine Seriendruckbereiche.

Diese Methode ignoriert dieRemoveUnusedRegions Möglichkeit.

### Beispiele

Zeigt, wie ein Bild aus einem URI als Seriendruckdaten in einem MERGEFIELD zusammengeführt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// MERGEFIELDs mit "Image:"-Tags erhalten beim Seriendruck ein Bild.
// Die Zeichenfolge nach dem Doppelpunkt im "Image:"-Tag entspricht einem Spaltennamen
// in der Datenquelle, deren Zellen URIs von Bilddateien enthalten.
builder.InsertField("MERGEFIELD  Image:logo_FromWeb ");
builder.InsertField("MERGEFIELD  Image:logo_FromFileSystem ");

 // Erstellen Sie eine Datenquelle, die URIs von Bildern enthält, die wir zusammenführen werden.
// Ein URI kann eine Web-URL sein, die auf ein Bild verweist, oder der Dateiname einer Bilddatei im lokalen Dateisystem.
string[] columns = { "logo_FromWeb", "logo_FromFileSystem" };
object[] URIs = { ImageUrl, ImageDir + "Logo.jpg" };

// Einen Seriendruck für eine Datenquelle mit einer Zeile ausführen.
doc.MailMerge.Execute(columns, URIs);

doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromUrl.docx");
```

Zeigt, wie Sie einen Seriendruck durchführen und das Dokument dann im Client-Browser speichern.

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
Assert.That(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null),
    Throws.TypeOf<ArgumentNullException>()); //Wird ausgelöst, weil HttpResponse im Test null ist.

// Wir müssen diese Antwort manuell schließen, um sicherzustellen, dass wir dem Dokument nach dem Speichern keine überflüssigen Inhalte hinzufügen.
Assert.That(() => response.End(), Throws.TypeOf<NullReferenceException>());
```

### Siehe auch

* class [MailMerge](../../mailmerge)
* namensraum [Aspose.Words.MailMerging](../../mailmerge)
* Montage [Aspose.Words](../../../)

---

## Execute(DataTable) {#execute_2}

Führt einen Seriendruck von einer DataTable in das Dokument durch.

```csharp
public void Execute(DataTable table)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| table | DataTable | Tabelle, die Daten enthält, die in Seriendruckfelder eingefügt werden sollen. Bei Feldnamen wird nicht zwischen Groß- und Kleinschreibung unterschieden. Wenn ein Feldname gefunden wird, der nicht im Dokument gefunden wird, wird er ignoriert. |

### Bemerkungen

Verwenden Sie diese Methode, um Seriendruckfelder im Dokument mit Werten aus a zu füllen. **Datentabelle**.

Alle Datensätze aus der Tabelle werden im Dokument zusammengeführt.

Sie können das NEXT-Feld im Word-Dokument verwenden, um dies zu bewirken **Seriendruck** Objekt zu select nächsten Datensatz aus dem **Datentabelle** und mit dem Zusammenführen fortfahren. Dies kann beim Erstellen von Dokumenten wie Adressetiketten verwendet werden.

Wann **Seriendruck**Objekt erreicht das Ende des Hauptdokuments und es gibt immer noch more Zeilen in der **Datentabelle**, kopiert es den gesamten Inhalt des Hauptdokuments und fügt ihn an das Ende des Zieldokuments an, wobei ein Abschnitt als Trennzeichen verwendet wird.

Diese Methode ignoriert dieRemoveUnusedRegions Möglichkeit.

### Beispiele

Zeigt, wie ein Seriendruck mit Daten aus einer DataTable ausgeführt wird.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Im Folgenden finden Sie zwei Möglichkeiten, eine DataTable als Datenquelle für einen Seriendruck zu verwenden.
    // 1 - Verwenden Sie die gesamte Tabelle für den Seriendruck, um ein Ausgabe-Seriendruckdokument für jede Zeile in der Tabelle zu erstellen:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Verwenden Sie eine Zeile der Tabelle, um ein Seriendruckdokument zu erstellen:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Erstellt ein Seriendruck-Quelldokument.
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

* class [MailMerge](../../mailmerge)
* namensraum [Aspose.Words.MailMerging](../../mailmerge)
* Montage [Aspose.Words](../../../)

---

## Execute(IDataReader) {#execute_4}

Führt den Seriendruck von IDataReader in das Dokument durch.

```csharp
public void Execute(IDataReader dataReader)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| dataReader | IDataReader | Datenquelle für den Seriendruckvorgang. |

### Bemerkungen

Du kannst passieren **SqlDataReader** oder **OleDbDataReader** Objekt in die Methode this als Parameter, da sie beide implementiert sind **IDataReader** Schnittstelle.

Beachten Sie, dass bei dieser Methode keine Seriendruckbereiche verwendet werden und bei mehreren Datensätzen das -Dokument wächst, indem das gesamte Dokument wiederholt wird.

Diese Methode ignoriert dieRemoveUnusedRegions Möglichkeit.

### Beispiele

Zeigt, wie Sie einen Seriendruck mit Daten aus einem Datenlesegerät ausführen.

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

// Erstellen Sie eine Verbindungszeichenfolge, die auf die Datenbankdatei "Northwind" zeigt
// Öffnen Sie in unserem lokalen Dateisystem eine Verbindung und richten Sie eine SQL-Abfrage ein.
string connectionString = @"Driver={Microsoft Access Driver (*.mdb)};Dbq=" + DatabaseDir + "Northwind.mdb";
string query = 
    @"SELECT Products.ProductName, Suppliers.CompanyName, Products.QuantityPerUnit, {fn ROUND(Products.UnitPrice,2)} as UnitPrice
    FROM Products 
    INNER JOIN Suppliers 
    ON Products.SupplierID = Suppliers.SupplierID";

using (OdbcConnection connection = new OdbcConnection())
{
    connection.ConnectionString = connectionString;
    connection.Open();

    // Erstellen Sie einen SQL-Befehl, der Daten für unseren Seriendruck liefert.
    // Die Namen der Spalten der Tabelle, die diese SELECT-Anweisung zurückgibt
    // muss den oben platzierten Zusammenführungsfeldern entsprechen.
    OdbcCommand command = connection.CreateCommand();
    command.CommandText = query;

    // Dies führt den Befehl aus und speichert die Daten im Lesegerät.
    OdbcDataReader reader = command.ExecuteReader(CommandBehavior.CloseConnection);

    // Daten aus dem Lesegerät übernehmen und im Seriendruck verwenden.
    doc.MailMerge.Execute(reader);
}

doc.Save(ArtifactsDir + "MailMerge.ExecuteDataReader.docx");
```

### Siehe auch

* class [MailMerge](../../mailmerge)
* namensraum [Aspose.Words.MailMerging](../../mailmerge)
* Montage [Aspose.Words](../../../)

---

## Execute(DataView) {#execute_3}

Führt einen Seriendruck von einer DataView in das Dokument durch.

```csharp
public void Execute(DataView dataView)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| dataView | DataView | Datenquelle für den Seriendruckvorgang. |

### Bemerkungen

Diese Methode ist nützlich, wenn Sie Daten in a abrufen **Datentabelle** aber then muss vor dem Seriendruck einen Filter oder eine Sortierung anwenden.

Beachten Sie, dass bei dieser Methode keine Seriendruckbereiche verwendet werden und bei mehreren Datensätzen das -Dokument wächst, indem das gesamte Dokument wiederholt wird.

Diese Methode ignoriert dieRemoveUnusedRegions Möglichkeit.

### Beispiele

Zeigt, wie Sie Seriendruckdaten mit einer DataView bearbeiten.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Congratulations ");
builder.InsertField(" MERGEFIELD Name");
builder.Write(" for passing with a grade of ");
builder.InsertField(" MERGEFIELD Grade");

// Erstellen Sie eine Datentabelle, aus der unser Seriendruck Daten bezieht.
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

* class [MailMerge](../../mailmerge)
* namensraum [Aspose.Words.MailMerging](../../mailmerge)
* Montage [Aspose.Words](../../../)

---

## Execute(DataRow) {#execute_1}

Führt einen Seriendruck von einer DataRow in das Dokument durch.

```csharp
public void Execute(DataRow row)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| row | DataRow | Zeile, die Daten enthält, die in Seriendruckfelder eingefügt werden sollen. Bei Feldnamen wird nicht zwischen Groß- und Kleinschreibung unterschieden. Wenn ein Feldname gefunden wird, der nicht im Dokument gefunden wird, wird er ignoriert. |

### Bemerkungen

Verwenden Sie diese Methode, um Serienbrieffelder im Dokument mit Werten aus a zu füllen **Datenzeile**.

Diese Methode ignoriert dieRemoveUnusedRegions Möglichkeit.

### Beispiele

Zeigt, wie ein Seriendruck mit Daten aus einer DataTable ausgeführt wird.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Im Folgenden finden Sie zwei Möglichkeiten, eine DataTable als Datenquelle für einen Seriendruck zu verwenden.
    // 1 - Verwenden Sie die gesamte Tabelle für den Seriendruck, um ein Ausgabe-Seriendruckdokument für jede Zeile in der Tabelle zu erstellen:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Verwenden Sie eine Zeile der Tabelle, um ein Seriendruckdokument zu erstellen:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Erstellt ein Seriendruck-Quelldokument.
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

* class [MailMerge](../../mailmerge)
* namensraum [Aspose.Words.MailMerging](../../mailmerge)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
