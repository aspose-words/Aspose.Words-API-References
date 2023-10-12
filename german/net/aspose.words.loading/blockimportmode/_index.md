---
title: Enum BlockImportMode
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Loading.BlockImportMode opsomming. Gibt an wie Eigenschaften von Elementen auf Blockebene aus HTMLbasierten Dokumenten importiert werden.
type: docs
weight: 3560
url: /de/net/aspose.words.loading/blockimportmode/
---
## BlockImportMode enumeration

Gibt an, wie Eigenschaften von Elementen auf Blockebene aus HTML-basierten Dokumenten importiert werden.

```csharp
public enum BlockImportMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Merge | `0` | Eigenschaften übergeordneter Blöcke werden zusammengeführt und in untergeordneten Elementen (z. B. Absätzen oder Tabellen) gespeichert. |
| Preserve | `1` | Eigenschaften übergeordneter Blöcke werden in eine spezielle logische Struktur importiert und getrennt von Dokumentknoten gespeichert. |

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

* namensraum [Aspose.Words.Loading](../../aspose.words.loading/)
* Montage [Aspose.Words](../../)


