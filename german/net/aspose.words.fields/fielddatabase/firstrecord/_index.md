---
title: FieldDatabase.FirstRecord
linktitle: FirstRecord
articleTitle: FirstRecord
second_title: Aspose.Words für .NET
description: Entdecken Sie die FirstRecord-Eigenschaft in FieldDatabase und verwalten Sie ganz einfach Ihre anfängliche Datensatznummer für eine nahtlose Dateneinfügung und verbesserte Effizienz.
type: docs
weight: 40
url: /de/net/aspose.words.fields/fielddatabase/firstrecord/
---
## FieldDatabase.FirstRecord property

Ruft die ganzzahlige Datensatznummer des ersten einzufügenden Datensatzes ab oder legt diese fest.

```csharp
public string FirstRecord { get; set; }
```

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

* class [FieldDatabase](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
