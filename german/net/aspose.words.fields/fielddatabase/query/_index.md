---
title: FieldDatabase.Query
second_title: Aspose.Words für .NET-API-Referenz
description: FieldDatabase eigendom. Ruft eine Reihe von SQLAnweisungen ab die die Datenbank abfragen oder legt diese fest.
type: docs
weight: 90
url: /de/net/aspose.words.fields/fielddatabase/query/
---
## FieldDatabase.Query property

Ruft eine Reihe von SQL-Anweisungen ab, die die Datenbank abfragen, oder legt diese fest.

```csharp
public string Query { get; set; }
```

### Beispiele

Zeigt, wie man Daten aus einer Datenbank extrahiert und als Feld in ein Dokument einfügt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Dieses DATABASE-Feld führt eine Abfrage in einer Datenbank aus und zeigt das Ergebnis in einer Tabelle an.
FieldDatabase field = (FieldDatabase)builder.InsertField(FieldType.FieldDatabase, true);
field.FileName = DatabaseDir + "Northwind.accdb";
field.Connection = "Provider=Microsoft.ACE.OLEDB.12.0";
field.Query = "SELECT * FROM [Products]";

Assert.AreEqual($" DATABASE  \\d {DatabaseDir.Replace("\\", "\\\\") + "Northwind.accdb"} \\c Provider=Microsoft.ACE.OLEDB.12.0 \\s \"SELECT * FROM [Products]\"", field.GetFieldCode());

// Ein weiteres DATABASE-Feld mit einer komplexeren Abfrage einfügen, die alle Produkte in absteigender Reihenfolge nach Bruttoumsatz sortiert.
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
// Konfigurieren Sie sie so, dass nur die Zeilen 1 bis 10 des Abfrageergebnisses in der Tabelle des Felds angezeigt werden.
field.FirstRecord = "1";
field.LastRecord = "10";

// Diese Eigenschaft ist der Index des Formats, das wir für unsere Tabelle verwenden möchten. Die Liste der Tabellenformate finden Sie im Menü „Table AutoFormat…“.
// das angezeigt wird, wenn wir ein DATABASE-Feld in Microsoft Word erstellen. Index Nr. 10 entspricht dem Format „Bunte 3“.
field.TableFormat = "10";

// Die FormatAttribute-Eigenschaft ist eine String-Darstellung einer Ganzzahl, die mehrere Flags speichert.
// Wir können das Format, auf das die TableFormat-Eigenschaft verweist, teilweise anwenden, indem wir in dieser Eigenschaft verschiedene Flags setzen.
// Die von uns verwendete Zahl ist die Summe einer Kombination von Werten, die verschiedenen Aspekten des Tabellenstils entsprechen.
// 63 steht für 1 (Ränder) + 2 (Schattierung) + 4 (Schriftart) + 8 (Farbe) + 16 (automatische Anpassung) + 32 (Überschriftenzeilen).
field.FormatAttributes = "63";
field.InsertHeadings = true;
field.InsertOnceOnMailMerge = true;

doc.FieldOptions.FieldDatabaseProvider = new OleDbFieldDatabaseProvider();
doc.UpdateFields();

doc.Save(ArtifactsDir + "Field.DATABASE.docx");
```

### Siehe auch

* class [FieldDatabase](../)
* namensraum [Aspose.Words.Fields](../../fielddatabase/)
* Montage [Aspose.Words](../../../)


