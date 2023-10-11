---
title: Enum BlockImportMode
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Loading.BlockImportMode uppräkning. Anger hur egenskaper för element på blocknivå importeras från HTMLbaserade dokument.
type: docs
weight: 3560
url: /sv/net/aspose.words.loading/blockimportmode/
---
## BlockImportMode enumeration

Anger hur egenskaper för element på blocknivå importeras från HTML-baserade dokument.

```csharp
public enum BlockImportMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Merge | `0` | Egenskaper för överordnade block slås samman och lagras i underordnade element (dvs. stycken eller tabeller). |
| Preserve | `1` | Egenskaper för överordnade block importeras till en speciell logisk struktur och lagras separat från dokumentnoder. |

### Exempel

Visar hur egenskaper för element på blocknivå importeras från HTML-baserade dokument.

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


