---
title: HtmlLoadOptions.BlockImportMode
linktitle: BlockImportMode
articleTitle: BlockImportMode
second_title: Aspose.Words für .NET
description: Entdecken Sie die BlockImportMode-Eigenschaft von HtmlLoadOptions, um den Import von Blockelementen anzupassen. Kontrollieren Sie die Zusammenführung für optimales Content-Management!
type: docs
weight: 20
url: /de/net/aspose.words.loading/htmlloadoptions/blockimportmode/
---
## HtmlLoadOptions.BlockImportMode property

Ruft einen Wert ab oder legt ihn fest, der angibt, wie Eigenschaften von Blockelementen importiert werden. Der Standardwert istMerge .

```csharp
public BlockImportMode BlockImportMode { get; set; }
```

## Beispiele

Zeigt, wie Eigenschaften von Blockelementen aus HTML-basierten Dokumenten importiert werden.

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
// Legen Sie den neuen Modus zum Importieren von HTML-Elementen auf Blockebene fest.
loadOptions.BlockImportMode = blockImportMode;

Document doc = new Document(stream, loadOptions);
doc.Save(ArtifactsDir + "HtmlLoadOptions.BlockImport.docx");
```

### Siehe auch

* enum [BlockImportMode](../../blockimportmode/)
* class [HtmlLoadOptions](../)
* namensraum [Aspose.Words.Loading](../../../aspose.words.loading/)
* Montage [Aspose.Words](../../../)
