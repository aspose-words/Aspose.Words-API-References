---
title: BlockImportMode Enum
linktitle: BlockImportMode
articleTitle: BlockImportMode
second_title: Aspose.Words för .NET
description: Upptäck hur enumerationen Aspose.Words.BlockImportMode förbättrar integrationen av HTML-dokument genom att optimera import av elementegenskaper på blocknivå för sömlösa arbetsflöden.
type: docs
weight: 4010
url: /sv/net/aspose.words.loading/blockimportmode/
---
## BlockImportMode enumeration

Anger hur egenskaper för blocknivåelement importeras från HTML-baserade dokument.

```csharp
public enum BlockImportMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Merge | `0` | Egenskaper för överordnade block slås samman och lagras på underordnade element (dvs. stycken eller tabeller). |
| Preserve | `1` | Egenskaper för överordnade block importeras till en speciell logisk struktur och lagras separat från dokumentnoder. |

## Exempel

Visar hur egenskaper för blocknivåelement importeras från HTML-baserade dokument.

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
MemoryStream stream = new MemoryStream(Encoding.UTF8.GetBytes(html));

HtmlLoadOptions loadOptions = new HtmlLoadOptions();
// Ställ in det nya läget för import av HTML-element på blocknivå.
loadOptions.BlockImportMode = blockImportMode;

Document doc = new Document(stream, loadOptions);
doc.Save(ArtifactsDir + "HtmlLoadOptions.BlockImport.docx");
```

### Se även

* namnutrymme [Aspose.Words.Loading](../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../)
