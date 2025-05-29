---
title: FieldDatabase Class
linktitle: FieldDatabase
articleTitle: FieldDatabase
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Fields.FieldDatabase för att effektivt implementera DATABASE-fält i dina dokument. Förbättra din dokumentautomation idag!
type: docs
weight: 2150
url: /sv/net/aspose.words.fields/fielddatabase/
---
## FieldDatabase class

Implementerar DATABAS-fältet.

För att lära dig mer, besök[Arbeta med fält](https://docs.aspose.com/words/net/working-with-fields/) dokumentationsartikel.

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
| [Connection](../../aspose.words.fields/fielddatabase/connection/) { get; set; } | Hämtar eller upprättar en koppling till data. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Hämtar texten som representerar det visade fältresultatet. |
| [End](../../aspose.words.fields/field/end/) { get; } | Hämtar noden som representerar fältets slut. |
| [FileName](../../aspose.words.fields/fielddatabase/filename/) { get; set; } | Hämtar eller anger den fullständiga sökvägen och filnamnet för databasen |
| [FirstRecord](../../aspose.words.fields/fielddatabase/firstrecord/) { get; set; } | Hämtar eller ställer in integralpostnumret för den första dataposten som ska infogas. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Får en[`FieldFormat`](../fieldformat/)objekt som ger typad åtkomst till fältets formatering. |
| [FormatAttributes](../../aspose.words.fields/fielddatabase/formatattributes/) { get; set; } | Hämtar eller anger vilka attribut för formatet som ska tillämpas på tabellen. |
| [InsertHeadings](../../aspose.words.fields/fielddatabase/insertheadings/) { get; set; } | Hämtar eller anger om fältnamnen från databasen ska infogas som kolumnrubriker i den resulterande tabellen. |
| [InsertOnceOnMailMerge](../../aspose.words.fields/fielddatabase/insertonceonmailmerge/) { get; set; } | Hämtar eller anger om data ska infogas i början av en sammanslagning. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Hämtar eller anger om fältet är låst (resultatet ska inte beräknas om). |
| [LastRecord](../../aspose.words.fields/fielddatabase/lastrecord/) { get; set; } | Hämtar eller ställer in integralpostnumret för den sista dataposten som ska infogas. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Hämtar eller ställer in fältets LCID. |
| [Query](../../aspose.words.fields/fielddatabase/query/) { get; set; } | Hämtar eller ställer in en uppsättning SQL-instruktioner som frågar databasen. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Hämtar eller anger text som är mellan fältavgränsaren och fältslutet. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Hämtar noden som representerar fältseparatorn. Kan vara`null` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Hämtar noden som representerar början av fältet. |
| [TableFormat](../../aspose.words.fields/fielddatabase/tableformat/) { get; set; } | Hämtar eller anger formatet som ska tillämpas på resultatet av databasfrågan. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Hämtar fälttypen Microsoft Word. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). Både fältkod och fältresultat för underfält inkluderas. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). |
| [Remove](../../aspose.words.fields/field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod direkt efter fältet. Om fältets slut är den sista undernoden till dess överordnade nod, returneras dess överordnade stycke. Om fältet redan är borttaget returneras`null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Utför fältavkopplingen. |
| [Update](../../aspose.words.fields/field/update/)() | Utför fältuppdateringen. Körs om fältet redan uppdateras. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Utför en fältuppdatering. Körs om fältet redan uppdateras. |

## Anmärkningar

Infogar resultatet av en databasfråga i en WordprocessingML-tabell.

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

* class [Field](../field/)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)
