---
title: FieldDatabase Class
linktitle: FieldDatabase
articleTitle: FieldDatabase
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words.Fields.FieldDatabase-Klasse, um DATABASE-Felder effizient in Ihre Dokumente zu implementieren. Verbessern Sie noch heute Ihre Dokumentenautomatisierung!
type: docs
weight: 2150
url: /de/net/aspose.words.fields/fielddatabase/
---
## FieldDatabase class

Implementiert das DATABASE-Feld.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Feldern](https://docs.aspose.com/words/net/working-with-fields/) Dokumentationsartikel.

```csharp
public class FieldDatabase : Field
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldDatabase](fielddatabase/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Connection](../../aspose.words.fields/fielddatabase/connection/) { get; set; } | Ruft eine Verbindung zu den Daten ab oder legt sie fest. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [FileName](../../aspose.words.fields/fielddatabase/filename/) { get; set; } | Ruft den vollständigen Pfad und Dateinamen der Datenbank ab oder legt ihn fest |
| [FirstRecord](../../aspose.words.fields/fielddatabase/firstrecord/) { get; set; } | Ruft die ganzzahlige Datensatznummer des ersten einzufügenden Datensatzes ab oder legt diese fest. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Erhält eine[`FieldFormat`](../fieldformat/)Objekt, das typisierten Zugriff auf die Formatierung des Felds bietet. |
| [FormatAttributes](../../aspose.words.fields/fielddatabase/formatattributes/) { get; set; } | Ruft ab oder legt fest, welche Attribute des Formats auf die Tabelle angewendet werden sollen. |
| [InsertHeadings](../../aspose.words.fields/fielddatabase/insertheadings/) { get; set; } | Ruft ab oder legt fest, ob die Feldnamen aus der Datenbank als Spaltenüberschriften in die resultierende Tabelle eingefügt werden sollen. |
| [InsertOnceOnMailMerge](../../aspose.words.fields/fielddatabase/insertonceonmailmerge/) { get; set; } | Ruft ab oder legt fest, ob am Anfang einer Zusammenführung Daten eingefügt werden sollen. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer am Dokument vorgenommener Änderungen nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (das Ergebnis sollte nicht neu berechnet werden). |
| [LastRecord](../../aspose.words.fields/fielddatabase/lastrecord/) { get; set; } | Ruft die ganzzahlige Datensatznummer des letzten einzufügenden Datensatzes ab oder legt diese fest. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [Query](../../aspose.words.fields/fielddatabase/query/) { get; set; } | Ruft einen Satz von SQL-Anweisungen ab, die die Datenbank abfragen, oder legt diesen fest. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ruft Text ab oder legt ihn fest, der zwischen Feldtrennzeichen und Feldende steht. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann sein`null` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| [TableFormat](../../aspose.words.fields/fielddatabase/tableformat/) { get; set; } | Ruft das Format ab oder legt es fest, das auf das Ergebnis der Datenbankabfrage angewendet werden soll. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ruft den Microsoft Word-Feldtyp ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldergebnis von untergeordneten Feldern werden einbezogen. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). |
| [Remove](../../aspose.words.fields/field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Felds das letzte Kind seines übergeordneten Knotens ist, wird dessen übergeordneter Absatz zurückgegeben. Wenn das Feld bereits entfernt wurde, wird zurückgegeben`null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Führt die Feldverknüpfung aus. |
| [Update](../../aspose.words.fields/field/update/)() | Führt die Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Führt eine Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |

## Bemerkungen

Fügt die Ergebnisse einer Datenbankabfrage in eine WordprocessingML-Tabelle ein.

## Beispiele

Zeigt, wie Daten aus einer Datenbank extrahiert und als Feld in ein Dokument eingefügt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Dieses DATABASE-Feld führt eine Abfrage einer Datenbank aus und zeigt das Ergebnis in einer Tabelle an.
FieldDatabase field = (FieldDatabase)builder.InsertField(FieldType.FieldDatabase, true);
field.FileName = DatabaseDir + "Northwind.accdb";
field.Connection = "Provider=Microsoft.ACE.OLEDB.12.0";
field.Query = "SELECT * FROM [Products]";

Assert.AreEqual($" DATABASE  \\d {DatabaseDir.Replace("\\", "\\\\") + "Northwind.accdb"} \\c Provider=Microsoft.ACE.OLEDB.12.0 \\s \"SELECT * FROM [Products]\"", field.GetFieldCode());

// Fügen Sie ein weiteres DATABASE-Feld mit einer komplexeren Abfrage ein, die alle Produkte in absteigender Reihenfolge nach Bruttoumsatz sortiert.
field = (FieldDatabase)builder.InsertField(FieldType.FieldDatabase, true);
field.FileName = DatabaseDir + "Northwind.accdb";
field.Connection = "Provider=Microsoft.ACE.OLEDB.12.0";
field.Query =
    "SELECT [Products].ProductName, FORMAT(SUM([Order Details].UnitPrice * (1 - [Order Details].Discount) * [Order Details].Quantity), 'Currency') AS GrossSales " +
    "FROM([Products] " +
    "LEFT JOIN[Order Details] ON[Products].[ProductID] = [Order Details].[ProductID]) " +
    "GROUP BY[Products].ProductName " +
    "ORDER BY SUM([Order Details].UnitPrice* (1 - [Order Details].Discount) * [Order Details].Quantity) DESC";

// Diese Eigenschaften haben die gleiche Funktion wie LIMIT- und TOP-Klauseln.
// Konfigurieren Sie sie so, dass in der Tabelle des Felds nur die Zeilen 1 bis 10 des Abfrageergebnisses angezeigt werden.
field.FirstRecord = "1";
field.LastRecord = "10";

// Diese Eigenschaft ist der Index des Formats, das wir für unsere Tabelle verwenden möchten. Die Liste der Tabellenformate finden Sie im Menü "Tabellen-AutoFormat..."
// das wird angezeigt, wenn wir ein DATABASE-Feld in Microsoft Word erstellen. Index Nr. 10 entspricht dem Format „Colorful 3“.
field.TableFormat = "10";

// Die Eigenschaft „FormatAttribute“ ist eine Zeichenfolgendarstellung einer Ganzzahl, die mehrere Flags speichert.
// Wir können das Format, auf das die Eigenschaft TableFormat verweist, teilweise anwenden, indem wir in dieser Eigenschaft verschiedene Flags setzen.
// Die von uns verwendete Zahl ist die Summe einer Kombination von Werten, die verschiedenen Aspekten des Tabellenstils entsprechen.
// 63 steht für 1 (Ränder) + 2 (Schattierung) + 4 (Schriftart) + 8 (Farbe) + 16 (Automatische Anpassung) + 32 (Überschriftenzeilen).
field.FormatAttributes = "63";
field.InsertHeadings = true;
field.InsertOnceOnMailMerge = true;

doc.FieldOptions.FieldDatabaseProvider = new OleDbFieldDatabaseProvider();
doc.UpdateFields();

doc.Save(ArtifactsDir + "Field.DATABASE.docx");
```

### Siehe auch

* class [Field](../field/)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)
