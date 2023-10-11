---
title: HtmlLoadOptions.BlockImportMode
second_title: Aspose.Words für .NET-API-Referenz
description: HtmlLoadOptions eigendom. Ruft einen Wert ab oder legt diesen fest der angibt wie Eigenschaften von Elementen auf Blockebene importiert werden. Der Standardwert istMerge .
type: docs
weight: 20
url: /de/net/aspose.words.loading/htmlloadoptions/blockimportmode/
---
## HtmlLoadOptions.BlockImportMode property

Ruft einen Wert ab oder legt diesen fest, der angibt, wie Eigenschaften von Elementen auf Blockebene importiert werden. Der Standardwert istMerge .

```csharp
public BlockImportMode BlockImportMode { get; set; }
```

### Beispiele

Zeigt, wie Eigenschaften von Elementen auf Blockebene aus HTML-basierten Dokumenten importiert werden.

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
// Legen Sie den neuen Modus für den Import von HTML-Elementen auf Blockebene fest.
loadOptions.BlockImportMode = blockImportMode;

Document doc = new Document(stream, loadOptions);
doc.Save(ArtifactsDir + "HtmlLoadOptions.BlockImport.docx");
```

### Siehe auch

* enum [BlockImportMode](../../blockimportmode/)
* class [HtmlLoadOptions](../)
* namensraum [Aspose.Words.Loading](../../htmlloadoptions/)
* Montage [Aspose.Words](../../../)


