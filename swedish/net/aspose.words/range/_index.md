---
title: Class Range
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Range klass. Representerar ett angränsande område i ett dokument.
type: docs
weight: 4520
url: /sv/net/aspose.words/range/
---
## Range class

Representerar ett angränsande område i ett dokument.

För att lära dig mer, besök[Arbeta med Ranges](https://docs.aspose.com/words/net/working-with-ranges/) dokumentationsartikel.

```csharp
public class Range
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Bookmarks](../../aspose.words/range/bookmarks/) { get; } | Returnerar en[`Bookmarks`](./bookmarks/) samling som representerar alla bokmärken i intervallet. |
| [Fields](../../aspose.words/range/fields/) { get; } | Returnerar en[`Fields`](./fields/) samling som representerar alla fält i området. |
| [FormFields](../../aspose.words/range/formfields/) { get; } | Returnerar en[`FormFields`](./formfields/) samling som representerar alla formulärfält i intervallet. |
| [Revisions](../../aspose.words/range/revisions/) { get; } | Hämtar en samling revisioner (spårade ändringar) som finns i detta intervall. |
| [StructuredDocumentTags](../../aspose.words/range/structureddocumenttags/) { get; } | Returnerar en[`StructuredDocumentTags`](./structureddocumenttags/) samling som representerar alla strukturerade dokumenttaggar i intervallet. |
| [Text](../../aspose.words/range/text/) { get; } | Hämtar intervallets text. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Delete](../../aspose.words/range/delete/)() | Tar bort alla tecken i intervallet. |
| [NormalizeFieldTypes](../../aspose.words/range/normalizefieldtypes/)() | Ändrar fälttypvärden[`FieldType`](../../aspose.words.fields/fieldchar/fieldtype/) av[`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../aspose.words.fields/fieldend/) i detta intervall så att de motsvarar fälttyperna som finns i fältkoderna. |
| [Replace](../../aspose.words/range/replace/#replace_2)(Regex, string) | Ersätter alla förekomster av ett teckenmönster som anges av ett reguljärt uttryck med en annan sträng. |
| [Replace](../../aspose.words/range/replace/#replace)(string, string) | Ersätter alla förekomster av ett specificerat teckensträngmönster med en ersättningssträng. |
| [Replace](../../aspose.words/range/replace/#replace_3)(Regex, string, FindReplaceOptions) | Ersätter alla förekomster av ett teckenmönster som anges av ett reguljärt uttryck med en annan sträng. |
| [Replace](../../aspose.words/range/replace/#replace_1)(string, string, FindReplaceOptions) | Ersätter alla förekomster av ett specificerat teckensträngmönster med en ersättningssträng. |
| [ToDocument](../../aspose.words/range/todocument/)() | Konstruerar ett nytt fullt format dokument som innehåller intervallet. |
| [UnlinkFields](../../aspose.words/range/unlinkfields/)() | Tar bort länkar till fält i det här intervallet. |
| [UpdateFields](../../aspose.words/range/updatefields/)() | Uppdaterar värdena för dokumentfält i detta intervall. |

### Anmärkningar

Dokumentet representeras av ett träd med noder och noderna tillhandahåller operations för att arbeta med trädet, men vissa operationer är lättare att utföra om dokument behandlas som en sammanhängande textsekvens.

`Range`är ett "fasad"-gränssnitt som tillhandahåller metoder som behandlar document eller delar av dokumentet som "platt" text oavsett det faktum att noderna document lagras i en trädliknande objektmodell.

`Range` innehåller ingen text eller noder, det är bara en vy eller "fönster" över ett fragment av ett dokument.

### Exempel

Visar hur man får fram textinnehållet för alla noder som ett intervall täcker.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.Range.Text.Trim());
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)


