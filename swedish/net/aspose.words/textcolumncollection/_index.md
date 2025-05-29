---
title: TextColumnCollection Class
linktitle: TextColumnCollection
articleTitle: TextColumnCollection
second_title: Aspose.Words för .NET
description: Utforska Aspose.Words.TextColumnCollection för att enkelt hantera textkolumner i dina dokument. Förbättra din dokumentformatering med lätthet!
type: docs
weight: 7250
url: /sv/net/aspose.words/textcolumncollection/
---
## TextColumnCollection class

En samling av[`TextColumn`](../textcolumn/) objekt som representerar alla textkolumner i ett avsnitt av ett dokument.

För att lära dig mer, besök[Arbeta med sektioner](https://docs.aspose.com/words/net/working-with-sections/) dokumentationsartikel.

```csharp
public class TextColumnCollection
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words/textcolumncollection/count/) { get; } | Hämtar antalet kolumner i avsnittet i ett dokument. |
| [EvenlySpaced](../../aspose.words/textcolumncollection/evenlyspaced/) { get; set; } | Sant om textkolumner har samma bredd och är jämnt fördelade. |
| [Item](../../aspose.words/textcolumncollection/item/) { get; } | Returnerar en textkolumn vid det angivna indexet. |
| [LineBetween](../../aspose.words/textcolumncollection/linebetween/) { get; set; } | När`sann` , lägger till en vertikal linje mellan kolumner. |
| [Spacing](../../aspose.words/textcolumncollection/spacing/) { get; set; } | När kolumnerna är jämnt fördelade, hämtar eller ställer in mängden avstånd mellan varje kolumn i punkter. |
| [Width](../../aspose.words/textcolumncollection/width/) { get; } | När kolumnerna är jämnt fördelade, hämtar kolumnernas bredd. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [SetCount](../../aspose.words/textcolumncollection/setcount/)(*int*) | Ordnar text i det angivna antalet textkolumner. |

## Anmärkningar

Använda[`SetCount`](./setcount/) för att ställa in antalet textkolumner.

För att göra alla kolumner lika breda och jämnt fördelade, ange[`EvenlySpaced`](./evenlyspaced/) till`sann` och ange mängden avstånd mellan kolumnerna i[`Spacing`](./spacing/)MS Word beräknar kolumnbredder automatiskt.

Om du har[`EvenlySpaced`](./evenlyspaced/) inställd på`falsk` , måste du ange bredd och avstånd för varje -kolumn individuellt. Använd indexeraren för att komma åt enskilda[`TextColumn`](../textcolumn/) föremål.

När du använder anpassade kolumnbredder, se till att summan av alla kolumnbredder och avstånden mellan dem är lika med sidbredden minus vänster och höger sidmarginaler.

## Exempel

Visar hur man skapar flera jämnt fördelade kolumner i ett avsnitt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.Spacing = 100;
columns.SetCount(2);

builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");

doc.Save(ArtifactsDir + "PageSetup.ColumnsSameWidth.docx");
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
