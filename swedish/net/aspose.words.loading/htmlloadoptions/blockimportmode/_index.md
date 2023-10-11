---
title: HtmlLoadOptions.BlockImportMode
second_title: Aspose.Words för .NET API Referens
description: HtmlLoadOptions fast egendom. Hämtar eller ställer in ett värde som anger hur egenskaper för element på blocknivå importeras. Standardvärdet ärMerge .
type: docs
weight: 20
url: /sv/net/aspose.words.loading/htmlloadoptions/blockimportmode/
---
## HtmlLoadOptions.BlockImportMode property

Hämtar eller ställer in ett värde som anger hur egenskaper för element på blocknivå importeras. Standardvärdet ärMerge .

```csharp
public BlockImportMode BlockImportMode { get; set; }
```

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

* enum [BlockImportMode](../../blockimportmode/)
* class [HtmlLoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../htmlloadoptions/)
* hopsättning [Aspose.Words](../../../)


