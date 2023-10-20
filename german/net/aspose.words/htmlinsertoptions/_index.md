---
title: HtmlInsertOptions Enum
linktitle: HtmlInsertOptions
articleTitle: HtmlInsertOptions
second_title: Aspose.Words für .NET
description: Aspose.Words.HtmlInsertOptions opsomming. Gibt Optionen für anInsertHtml method in C#.
type: docs
weight: 3140
url: /de/net/aspose.words/htmlinsertoptions/
---
## HtmlInsertOptions enumeration

Gibt Optionen für an[`InsertHtml`](../documentbuilder/inserthtml/) method.

```csharp
[Flags]
public enum HtmlInsertOptions
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Verwenden Sie beim Einfügen von HTML die Standardoptionen. |
| UseBuilderFormatting | `1` | Verwenden Sie die in angegebene Schriftart und Absatzformatierung[`DocumentBuilder`](../documentbuilder/) als Basisformatierung für aus HTML eingefügter Text . |
| RemoveLastEmptyParagraph | `2` | Entfernen Sie den leeren Absatz, der normalerweise nach HTML eingefügt wird und mit einem Element auf Blockebene endet. |
| PreserveBlocks | `4` | Eigenschaften von Elementen auf Blockebene beibehalten. |

## Beispiele

Zeigt, wie Sie die sichtbaren Ränder und Ränder besser erhalten können.

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

// Legen Sie den neuen Modus für den Import von HTML-Elementen auf Blockebene fest.
HtmlInsertOptions insertOptions = HtmlInsertOptions.PreserveBlocks;

DocumentBuilder builder = new DocumentBuilder();
builder.InsertHtml(html, insertOptions);
builder.Document.Save(ArtifactsDir + "DocumentBuilder.PreserveBlocks.docx");
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
