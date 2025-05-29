---
title: Range Class
linktitle: Range
articleTitle: Range
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Range, din nyckel till att hantera dokumentavsnitt utan ansträngning. Förbättra din dokumenthantering med sömlös kontroll och flexibilitet.
type: docs
weight: 5250
url: /sv/net/aspose.words/range/
---
## Range class

Representerar ett sammanhängande område i ett dokument.

För att lära dig mer, besök[Arbeta med intervall](https://docs.aspose.com/words/net/working-with-ranges/) dokumentationsartikel.

```csharp
public class Range : IEnumerable<Node>
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Bookmarks](../../aspose.words/range/bookmarks/) { get; } | Returnerar en[`Bookmarks`](./bookmarks/) samling som representerar alla bokmärken i intervallet. |
| [Fields](../../aspose.words/range/fields/) { get; } | Returnerar en[`Fields`](./fields/) samling som representerar alla fält i intervallet. |
| [FormFields](../../aspose.words/range/formfields/) { get; } | Returnerar en[`FormFields`](./formfields/) samling som representerar alla formulärfält i intervallet. |
| [Revisions](../../aspose.words/range/revisions/) { get; } | Hämtar en samling revisioner (spårade ändringar) som finns inom detta intervall. |
| [StructuredDocumentTags](../../aspose.words/range/structureddocumenttags/) { get; } | Returnerar en[`StructuredDocumentTags`](./structureddocumenttags/) samling som representerar alla strukturerade dokumenttaggar i intervallet. |
| [Text](../../aspose.words/range/text/) { get; } | Hämtar texten i intervallet. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Delete](../../aspose.words/range/delete/)() | Tar bort alla tecken i intervallet. |
| [GetEnumerator](../../aspose.words/range/getenumerator/)() |  |
| [NormalizeFieldTypes](../../aspose.words/range/normalizefieldtypes/)() | Ändrar fälttypvärden[`FieldType`](../../aspose.words.fields/fieldchar/fieldtype/) av[`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../aspose.words.fields/fieldend/) i detta intervall så att de motsvarar fälttyperna som finns i fältkoderna. |
| [Replace](../../aspose.words/range/replace/#replace_2)(*Regex, string*) | Ersätter alla förekomster av ett teckenmönster som anges av ett reguljärt uttryck med en annan sträng. |
| [Replace](../../aspose.words/range/replace/#replace)(*string, string*) | Ersätter alla förekomster av ett angivet teckensträngmönster med en ersättningssträng. |
| [Replace](../../aspose.words/range/replace/#replace_3)(*Regex, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | Ersätter alla förekomster av ett teckenmönster som anges av ett reguljärt uttryck med en annan sträng. |
| [Replace](../../aspose.words/range/replace/#replace_1)(*string, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | Ersätter alla förekomster av ett angivet teckensträngmönster med en ersättningssträng. |
| [ToDocument](../../aspose.words/range/todocument/)() | Skapar ett nytt fullständigt dokument som innehåller intervallet. |
| [UnlinkFields](../../aspose.words/range/unlinkfields/)() | Avlänkar fält i detta intervall. |
| [UpdateFields](../../aspose.words/range/updatefields/)() | Uppdaterar värdena för dokumentfält i detta intervall. |

## Anmärkningar

Dokumentet representeras av ett träd av noder och noderna tillhandahåller operationer för att arbeta med trädet, men vissa operationer är enklare att utföra om dokument behandlas som en sammanhängande textsekvens.

`Range` är ett "fasadgränssnitt" som tillhandahåller metoder som behandlar document eller delar av dokumentet som "platt" text oavsett det faktum att document -noderna lagras i en trädliknande objektmodell.

`Range` innehåller ingen text eller noder, det är bara en vy eller ett "fönster" över ett fragment av ett dokument.

## Exempel

Visar hur man hämtar textinnehållet för alla noder som ett område täcker.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.Range.Text.Trim());
```

### Se även

* class [Node](../node/)
* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
