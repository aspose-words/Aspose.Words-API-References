---
title: BlockImportMode Enum
linktitle: BlockImportMode
articleTitle: BlockImportMode
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Aufzählung Aspose.Words.BlockImportMode die Integration von HTML-Dokumenten verbessert, indem sie den Import von Elementeigenschaften auf Blockebene für nahtlose Arbeitsabläufe optimiert.
type: docs
weight: 4010
url: /de/net/aspose.words.loading/blockimportmode/
---
## BlockImportMode enumeration

Gibt an, wie Eigenschaften von Blockelementen aus HTML-basierten Dokumenten importiert werden.

```csharp
public enum BlockImportMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Merge | `0` | Eigenschaften von übergeordneten Blöcken werden zusammengeführt und in untergeordneten Elementen (z. B. Absätzen oder Tabellen) gespeichert. |
| Preserve | `1` | Eigenschaften von übergeordneten Blöcken werden in eine spezielle logische Struktur importiert und getrennt von Dokumentknoten gespeichert. |

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

* namensraum [Aspose.Words.Loading](../../aspose.words.loading/)
* Montage [Aspose.Words](../../)
