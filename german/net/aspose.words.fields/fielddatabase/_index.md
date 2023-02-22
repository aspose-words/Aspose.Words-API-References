---
title: Class FieldDatabase
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Fields.FieldDatabase klas. Implementiert das DATABASEFeld.
type: docs
weight: 1590
url: /de/net/aspose.words.fields/fielddatabase/
---
## FieldDatabase class

Implementiert das DATABASE-Feld.

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
| [Connection](../../aspose.words.fields/fielddatabase/connection/) { get; set; } | Ruft eine Verbindung zu den Daten ab oder stellt sie her. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [FileName](../../aspose.words.fields/fielddatabase/filename/) { get; set; } | Holt oder setzt den vollständigen Pfad und Dateinamen der Datenbank |
| [FirstRecord](../../aspose.words.fields/fielddatabase/firstrecord/) { get; set; } | Liest oder setzt die ganzzahlige Satznummer des ersten einzufügenden Datensatzes. |
| [Format](../../aspose.words.fields/field/format/) { get; } | erhält a[`FieldFormat`](../fieldformat/) Objekt, das typisierten Zugriff auf die Feldformatierung bereitstellt. |
| [FormatAttributes](../../aspose.words.fields/fielddatabase/formatattributes/) { get; set; } | Ermittelt oder setzt, welche Attribute des Formats auf die Tabelle angewendet werden sollen. |
| [InsertHeadings](../../aspose.words.fields/fielddatabase/insertheadings/) { get; set; } | Ruft ab oder legt fest, ob die Feldnamen aus der Datenbank als Spaltenüberschriften in der resultierenden Tabelle eingefügt werden sollen. |
| [InsertOnceOnMailMerge](../../aspose.words.fields/fielddatabase/insertonceonmailmerge/) { get; set; } | Ruft ab oder legt fest, ob Daten am Anfang einer Zusammenführung eingefügt werden sollen. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (sollte sein Ergebnis nicht neu berechnen). |
| [LastRecord](../../aspose.words.fields/fielddatabase/lastrecord/) { get; set; } | Holt oder setzt die ganzzahlige Satznummer des letzten einzufügenden Datensatzes. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [Query](../../aspose.words.fields/fielddatabase/query/) { get; set; } | Ruft eine Reihe von SQL-Anweisungen ab oder legt sie fest, die die Datenbank abfragen. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Liest oder setzt Text, der zwischen dem Feldtrennzeichen und dem Feldende steht. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann null sein. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| [TableFormat](../../aspose.words.fields/fielddatabase/tableformat/) { get; set; } | Holt oder setzt das Format, das auf das Ergebnis der Datenbankabfrage angewendet werden soll. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ruft den Microsoft Word-Feldtyp ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldergebnis von untergeordneten Feldern sind enthalten. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Gibt Text zwischen Feldanfang und Feldtrennzeichen (oder Feldende, wenn kein Trennzeichen vorhanden ist) zurück. |
| [Remove](../../aspose.words.fields/field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Felds das letzte Kind seines Elternknotens ist, wird sein Elternabsatz zurückgegeben. Wenn das Feld bereits entfernt wurde, wird zurückgegeben **Null** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Führt das Feld Unlink aus. |
| [Update](../../aspose.words.fields/field/update/)() | Führt die Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Führt eine Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |

### Bemerkungen

Fügt die Ergebnisse einer Datenbankabfrage in eine WordprocessingML-Tabelle ein.

### Beispiele

Zeigt, wie Daten aus einer Datenbank extrahiert und als Feld in ein Dokument eingefügt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Dieses DATABASE-Feld führt eine Abfrage in einer Datenbank aus und zeigt das Ergebnis in einer Tabelle an.
FieldDatabase field = (FieldDatabase)builder.InsertField(FieldType.FieldDatabase, true);
field.FileName = MyDir + @"Database\Northwind.mdb";
field.Connection = "DSN=MS Access Databases";
field.Query = "SELECT * FROM [Products]";

Assert.AreEqual($" DATABASE  \\d \"{DatabaseDir.Replace("\\", "\\\\") + "Northwind.mdb"}\" \\c \"DSN=MS Access Databases\" \\s \"SELECT * FROM [Products]\"", 
    field.GetFieldCode());

// Fügen Sie ein weiteres DATABASE-Feld mit einer komplexeren Abfrage ein, die alle Produkte in absteigender Reihenfolge nach Bruttoumsatz sortiert.
field = (FieldDatabase)builder.InsertField(FieldType.FieldDatabase, true);
field.FileName = MyDir + @"Database\Northwind.mdb";
field.Connection = "DSN=MS Access Databases";
field.Query =
    "SELECT [Products].ProductName, FORMAT(SUM([Order Details].UnitPrice * (1 - [Order Details].Discount) * [Order Details].Quantity), 'Currency') AS GrossSales " +
    "FROM([Products] " +
    "LEFT JOIN[Order Details] ON[Products].[ProductID] = [Order Details].[ProductID]) " +
    "GROUP BY[Products].ProductName " +
    "ORDER BY SUM([Order Details].UnitPrice* (1 - [Order Details].Discount) * [Order Details].Quantity) DESC";

// Diese Eigenschaften haben dieselbe Funktion wie LIMIT- und TOP-Klauseln.
// Konfigurieren Sie sie so, dass nur die Zeilen 1 bis 10 des Abfrageergebnisses in der Tabelle des Felds angezeigt werden.
field.FirstRecord = "1";
field.LastRecord = "10";

// Diese Eigenschaft ist der Index des Formats, das wir für unsere Tabelle verwenden möchten. Die Liste der Tabellenformate befindet sich im Menü "Tabellen-AutoFormat...".
// das erscheint, wenn wir ein DATENBANK-Feld in Microsoft Word erstellen. Index #10 entspricht dem Format „Bunte 3“.
field.TableFormat = "10";

// Die Eigenschaft FormatAttribute ist eine Zeichenfolgendarstellung einer Ganzzahl, die mehrere Flags speichert.
// Wir können das Format, auf das die TableFormat-Eigenschaft zeigt, partiell anwenden, indem wir verschiedene Flags in dieser Eigenschaft setzen.
// Die von uns verwendete Zahl ist die Summe einer Kombination von Werten, die verschiedenen Aspekten des Tabellenstils entsprechen.
// 63 steht für 1 (Rahmen) + 2 (Schattierung) + 4 (Schriftart) + 8 (Farbe) + 16 (Autofit) + 32 (Überschriftenzeilen).
field.FormatAttributes = "63";
field.InsertHeadings = true;
field.InsertOnceOnMailMerge = true;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.DATABASE.docx");
```

### Siehe auch

* class [Field](../field/)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)


