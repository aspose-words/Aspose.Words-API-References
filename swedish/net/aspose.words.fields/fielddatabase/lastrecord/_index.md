---
title: FieldDatabase.LastRecord
second_title: Aspose.Words för .NET API Referens
description: FieldDatabase fast egendom. Hämtar eller ställer in integralpostnumret för den senaste dataposten som ska infogas.
type: docs
weight: 80
url: /sv/net/aspose.words.fields/fielddatabase/lastrecord/
---
## FieldDatabase.LastRecord property

Hämtar eller ställer in integralpostnumret för den senaste dataposten som ska infogas.

```csharp
public string LastRecord { get; set; }
```

### Exempel

Visar hur man extraherar data från en databas och infogar den som ett fält i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Detta DATABAS-fält kommer att köra en fråga på en databas och visa resultatet i en tabell.
FieldDatabase field = (FieldDatabase)builder.InsertField(FieldType.FieldDatabase, true);
field.FileName = MyDir + @"Database\Northwind.mdb";
field.Connection = "DSN=MS Access Databases";
field.Query = "SELECT * FROM [Products]";

Assert.AreEqual($" DATABASE  \\d \"{DatabaseDir.Replace("\\", "\\\\") + "Northwind.mdb"}\" \\c \"DSN=MS Access Databases\" \\s \"SELECT * FROM [Products]\"", 
    field.GetFieldCode());

// Infoga ett annat DATABAS-fält med en mer komplex fråga som sorterar alla produkter i fallande ordning efter bruttoförsäljning.
field = (FieldDatabase)builder.InsertField(FieldType.FieldDatabase, true);
field.FileName = MyDir + @"Database\Northwind.mdb";
field.Connection = "DSN=MS Access Databases";
field.Query =
    "SELECT [Products].ProductName, FORMAT(SUM([Order Details].UnitPrice * (1 - [Order Details].Discount) * [Order Details].Quantity), 'Currency') AS GrossSales " +
    "FROM([Products] " +
    "LEFT JOIN[Order Details] ON[Products].[ProductID] = [Order Details].[ProductID]) " +
    "GROUP BY[Products].ProductName " +
    "ORDER BY SUM([Order Details].UnitPrice* (1 - [Order Details].Discount) * [Order Details].Quantity) DESC";

// Dessa egenskaper har samma funktion som LIMIT- och TOP-satser.
// Konfigurera dem för att endast visa raderna 1 till 10 i frågeresultatet i fältets tabell.
field.FirstRecord = "1";
field.LastRecord = "10";

// Den här egenskapen är indexet för formatet vi vill använda för vår tabell. Listan över tabellformat finns i menyn "Tabell AutoFormat...".
// som dyker upp när vi skapar ett DATABAS-fält i Microsoft Word. Index #10 motsvarar formatet "Colorful 3".
field.TableFormat = "10";

// Egenskapen FormatAttribute är en strängrepresentation av ett heltal som lagrar flera flaggor.
// Vi kan tillämpa formatet som TableFormat-egenskapen pekar på genom att sätta olika flaggor i den här egenskapen.
// Siffran vi använder är summan av en kombination av värden som motsvarar olika aspekter av tabellstilen.
// 63 representerar 1 (kanter) + 2 (skuggning) + 4 (teckensnitt) + 8 (färg) + 16 (autopassning) + 32 (rubriker).
field.FormatAttributes = "63";
field.InsertHeadings = true;
field.InsertOnceOnMailMerge = true;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.DATABASE.docx");
```

### Se även

* class [FieldDatabase](../)
* namnutrymme [Aspose.Words.Fields](../../fielddatabase/)
* hopsättning [Aspose.Words](../../../)


