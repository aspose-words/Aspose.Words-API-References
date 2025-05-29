---
title: HtmlInsertOptions Enum
linktitle: HtmlInsertOptions
articleTitle: HtmlInsertOptions
second_title: Aspose.Words für .NET
description: Erkunden Sie die Aufzählung Aspose.Words.HtmlInsertOptions, um die HTML-Einfügung mit der Methode InsertHtml anzupassen und so die Effizienz der Dokumentverarbeitung zu verbessern.
type: docs
weight: 3570
url: /de/net/aspose.words/htmlinsertoptions/
---
## HtmlInsertOptions enumeration

Gibt Optionen für die[`InsertHtml`](../documentbuilder/inserthtml/) Methode.

```csharp
[Flags]
public enum HtmlInsertOptions
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Verwenden Sie beim Einfügen von HTML die Standardoptionen. |
| UseBuilderFormatting | `1` | Verwenden Sie die Schriftart und Absatzformatierung, die in[`DocumentBuilder`](../documentbuilder/) als Basisformatierung für aus HTML eingefügten Text . |
| RemoveLastEmptyParagraph | `2` | Entfernen Sie den leeren Absatz, der normalerweise nach HTML eingefügt wird, das mit einem Blockelement endet. |
| PreserveBlocks | `4` | Bewahrt die Eigenschaften von Blockelementen. |

## Beispiele

Zeigt, wie sichtbare Grenzen und Ränder besser erhalten bleiben.

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

// Legen Sie den neuen Modus zum Importieren von HTML-Elementen auf Blockebene fest.
HtmlInsertOptions insertOptions = HtmlInsertOptions.PreserveBlocks;

DocumentBuilder builder = new DocumentBuilder();
builder.InsertHtml(html, insertOptions);
builder.Document.Save(ArtifactsDir + "DocumentBuilder.PreserveBlocks.docx");
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
