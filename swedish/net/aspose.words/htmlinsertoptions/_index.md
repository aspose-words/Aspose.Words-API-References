---
title: HtmlInsertOptions Enum
linktitle: HtmlInsertOptions
articleTitle: HtmlInsertOptions
second_title: Aspose.Words för .NET
description: Aspose.Words.HtmlInsertOptions uppräkning. Anger alternativ förInsertHtml metod i C#.
type: docs
weight: 3140
url: /sv/net/aspose.words/htmlinsertoptions/
---
## HtmlInsertOptions enumeration

Anger alternativ för[`InsertHtml`](../documentbuilder/inserthtml/) metod.

```csharp
[Flags]
public enum HtmlInsertOptions
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` | Använd standardalternativen när du infogar HTML. |
| UseBuilderFormatting | `1` | Använd teckensnitt och styckeformatering som anges i[`DocumentBuilder`](../documentbuilder/) som basformatering för text infogat från HTML. |
| RemoveLastEmptyParagraph | `2` | Ta bort det tomma stycket som normalt infogas efter HTML som slutar med ett element på blocknivå. |
| PreserveBlocks | `4` | Bevara egenskaperna för element på blocknivå. |

## Exempel

Visar hur man gör det möjligt att bättre bevara kanter och marginaler.

```csharp
const string html = @"
    <html>
        <div style='border:dotted'>
        <div style='border:solid'>
            <p>paragraph 1</p>
            <p>paragraph 2</p>
        </div>
        </div>
    </html>";

// Ställ in det nya läget för import av HTML-element på blocknivå.
HtmlInsertOptions insertOptions = HtmlInsertOptions.PreserveBlocks;

DocumentBuilder builder = new DocumentBuilder();
builder.InsertHtml(html, insertOptions);
builder.Document.Save(ArtifactsDir + "DocumentBuilder.PreserveBlocks.docx");
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
