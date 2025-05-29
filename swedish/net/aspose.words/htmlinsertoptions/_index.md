---
title: HtmlInsertOptions Enum
linktitle: HtmlInsertOptions
articleTitle: HtmlInsertOptions
second_title: Aspose.Words för .NET
description: Utforska Aspose.Words.HtmlInsertOptions enum för att anpassa HTML-infogning med InsertHtml-metoden, vilket förbättrar effektiviteten i dokumentbehandlingen.
type: docs
weight: 3570
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
| None | `0` | Använd standardinställningarna när du infogar HTML. |
| UseBuilderFormatting | `1` | Använd teckensnitt och styckeformatering som anges i[`DocumentBuilder`](../documentbuilder/) som basformatering för text infogad från HTML. |
| RemoveLastEmptyParagraph | `2` | Ta bort det tomma stycket som normalt infogas efter HTML och som slutar med ett blocknivåelement. |
| PreserveBlocks | `4` | Bevara egenskaper för element på blocknivå. |

## Exempel

Visar hur man bättre bevarar synliga kanter och marginaler.

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
