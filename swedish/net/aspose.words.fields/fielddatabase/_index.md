---
title: FieldDatabase Class
linktitle: FieldDatabase
articleTitle: FieldDatabase
second_title: Aspose.Words för .NET
description: Aspose.Words.Fields.FieldDatabase klass. Implementerar fältet DATABAS i C#.
type: docs
weight: 1740
url: /sv/net/aspose.words.fields/fielddatabase/
---
## FieldDatabase class

Implementerar fältet DATABAS.

För att lära dig mer, besök[Arbeta med Fields](https://docs.aspose.com/words/net/working-with-fields/) dokumentationsartikel.

```csharp
public class FieldDatabase : Field
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FieldDatabase](fielddatabase/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Connection](../../aspose.words.fields/fielddatabase/connection/) { get; set; } | Hämtar eller ställer in en anslutning till datan. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Hämtar texten som representerar det visade fältresultatet. |
| [End](../../aspose.words.fields/field/end/) { get; } | Hämtar noden som representerar fältänden. |
| [FileName](../../aspose.words.fields/fielddatabase/filename/) { get; set; } | Hämtar eller ställer in hela sökvägen och filnamnet för databasen |
| [FirstRecord](../../aspose.words.fields/fielddatabase/firstrecord/) { get; set; } | Hämtar eller ställer in integralpostnumret för den första dataposten som ska infogas. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Får en[`FieldFormat`](../fieldformat/) objekt som ger maskinskriven åtkomst till fältets formatering. |
| [FormatAttributes](../../aspose.words.fields/fielddatabase/formatattributes/) { get; set; } | Hämtar eller ställer in vilka attribut av formatet som ska tillämpas på tabellen. |
| [InsertHeadings](../../aspose.words.fields/fielddatabase/insertheadings/) { get; set; } | Hämtar eller ställer in om fältnamnen från databasen ska infogas som kolumnrubriker i den resulterande tabellen. |
| [InsertOnceOnMailMerge](../../aspose.words.fields/fielddatabase/insertonceonmailmerge/) { get; set; } | Hämtar eller ställer in om data ska infogas i början av en sammanslagning. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Hämtar eller ställer in om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Hämtar eller ställer in om fältet är låst (ska inte räkna om resultatet). |
| [LastRecord](../../aspose.words.fields/fielddatabase/lastrecord/) { get; set; } | Hämtar eller ställer in integralpostnumret för den senaste dataposten som ska infogas. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Hämtar eller ställer in LCID för fältet. |
| [Query](../../aspose.words.fields/fielddatabase/query/) { get; set; } | Hämtar eller ställer in en uppsättning SQL-instruktioner som frågar databasen. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Hämtar eller ställer in text som är mellan fältavgränsaren och fältslutet. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Hämtar noden som representerar fältseparatorn. Kan vara`null` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Hämtar noden som representerar början av fältet. |
| [TableFormat](../../aspose.words.fields/fielddatabase/tableformat/) { get; set; } | Hämtar eller ställer in formatet som ska tillämpas på resultatet av databasfrågan. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Hämtar fälttypen Microsoft Word. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). Både fältkod och fältresultat för underordnade fält ingår. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). |
| [Remove](../../aspose.words.fields/field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod direkt efter fältet. Om fältets slut är den sista child av dess överordnade nod, returnerar dess överordnade stycke. Om fältet redan är borttaget, returneras`null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Utför fältavlänkningen. |
| [Update](../../aspose.words.fields/field/update/)() | Utför fältuppdateringen. Kastar om fältet redan uppdateras. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Utför en fältuppdatering. Kastar om fältet redan uppdateras. |

## Anmärkningar

Infogar resultaten av en databasfråga i en WordprocessingML-tabell.

## Exempel

Visar hur man extraherar data från en databas och infogar den som ett fält i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Detta DATABAS-fält kommer att köra en fråga på en databas och visa resultatet i en tabell.
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

doc.FieldOptions.FieldDatabaseProvider = new OleDbFieldDatabaseProvider();
doc.UpdateFields();

doc.Save(ArtifactsDir + "Field.DATABASE.docx");
```

### Se även

* class [Field](../field/)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)
