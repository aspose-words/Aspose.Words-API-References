---
title: FieldDatabase.LastRecord
linktitle: LastRecord
articleTitle: LastRecord
second_title: Aspose.Words för .NET
description: Upptäck egenskapen LastRecord i FieldDatabase. Hantera enkelt ditt senaste datapostnummer för sömlös datainsättning och förbättrad databaseffektivitet.
type: docs
weight: 80
url: /sv/net/aspose.words.fields/fielddatabase/lastrecord/
---
## FieldDatabase.LastRecord property

Hämtar eller ställer in integralpostnumret för den sista dataposten som ska infogas.

```csharp
public string LastRecord { get; set; }
```

## Exempel

Visar hur man extraherar data från en databas och infogar den som ett fält i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Detta DATABASFÄLT kör en fråga i en databas och visar resultatet i en tabell.
FieldDatabase field = (FieldDatabase)builder.InsertField(FieldType.FieldDatabase, true);
field.FileName = DatabaseDir + "Northwind.accdb";
field.Connection = "Provider=Microsoft.ACE.OLEDB.12.0";
field.Query = "SELECT * FROM [Products]";

Assert.AreEqual($" DATABASE  \\d {DatabaseDir.Replace("\\", "\\\\") + "Northwind.accdb"} \\c Provider=Microsoft.ACE.OLEDB.12.0 \\s \"SELECT * FROM [Products]\"", field.GetFieldCode());

// Infoga ett annat DATABAS-fält med en mer komplex fråga som sorterar alla produkter i fallande ordning efter bruttoförsäljning.
field = (FieldDatabase)builder.InsertField(FieldType.FieldDatabase, true);
field.FileName = DatabaseDir + "Northwind.accdb";
field.Connection = "Provider=Microsoft.ACE.OLEDB.12.0";
field.Query =
    "SELECT [Products].ProductName, FORMAT(SUM([Order Details].UnitPrice * (1 - [Order Details].Discount) * [Order Details].Quantity), 'Currency') AS GrossSales " +
    "FROM([Products] " +
    "LEFT JOIN[Order Details] ON[Products].[ProductID] = [Order Details].[ProductID]) " +
    "GROUP BY[Products].ProductName " +
    "ORDER BY SUM([Order Details].UnitPrice* (1 - [Order Details].Discount) * [Order Details].Quantity) DESC";

// Dessa egenskaper har samma funktion som LIMIT- och TOP-klausulerna.
// Konfigurera dem så att endast raderna 1 till 10 av frågeresultatet visas i fältets tabell.
field.FirstRecord = "1";
field.LastRecord = "10";

// Den här egenskapen är indexet för det format vi vill använda för vår tabell. Listan över tabellformat finns i menyn "Tabellautoformat..."
// som visas när vi skapar ett DATABAS-fält i Microsoft Word. Index #10 motsvarar formatet "Colorful 3".
field.TableFormat = "10";

// Egenskapen FormatAttribute är en strängrepresentation av ett heltal som lagrar flera flaggor.
// Vi kan patriellt tillämpa formatet som egenskapen TableFormat pekar på genom att sätta olika flaggor i den här egenskapen.
// Talet vi använder är summan av en kombination av värden som motsvarar olika aspekter av tabellstilen.
// 63 representerar 1 (kantlinjer) + 2 (skuggning) + 4 (teckensnitt) + 8 (färg) + 16 (autoanpassning) + 32 (rubrikrader).
field.FormatAttributes = "63";
field.InsertHeadings = true;
field.InsertOnceOnMailMerge = true;

doc.FieldOptions.FieldDatabaseProvider = new OleDbFieldDatabaseProvider();
doc.UpdateFields();

doc.Save(ArtifactsDir + "Field.DATABASE.docx");
```

### Se även

* class [FieldDatabase](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
