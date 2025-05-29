---
title: EmphasisMark Enum
linktitle: EmphasisMark
articleTitle: EmphasisMark
second_title: Aspose.Words für .NET
description: Entdecken Sie Aspose.Words.EmphasisMark enum mit verschiedenen Hervorhebungsarten zur Verbesserung Ihrer Dokumentformatierung. Steigern Sie noch heute die Wirkung Ihres Textes!
type: docs
weight: 1870
url: /de/net/aspose.words/emphasismark/
---
## EmphasisMark enumeration

Gibt mögliche Arten von Hervorhebungszeichen an.

```csharp
public enum EmphasisMark
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Kein Hervorhebungszeichen. |
| OverSolidCircle | `1` | Das Hervorhebungszeichen ist ein ausgefüllter schwarzer Kreis, der über dem Text angezeigt wird. |
| OverComma | `2` | Hervorhebungszeichen ist ein Kommazeichen, das über dem Text angezeigt wird. |
| OverWhiteCircle | `3` | Das Hervorhebungszeichen ist ein leerer weißer Kreis, der über dem Text angezeigt wird. |
| UnderSolidCircle | `4` | Das Hervorhebungszeichen ist ein ausgefüllter schwarzer Kreis, der unter dem Text angezeigt wird. |

## Beispiele

Zeigt, wie zusätzliche Zeichen hinzugefügt werden, die über/unter dem Glyphenzeichen dargestellt werden.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// Mögliche Arten von Hervorhebungszeichen:
// https://apireference.aspose.com/words/net/aspose.words/emphasismark
builder.Font.EmphasisMark = emphasisMark; 

builder.Write("Emphasis text");
builder.Writeln();
builder.Font.ClearFormatting();
builder.Write("Simple text");

builder.Document.Save(ArtifactsDir + "Fonts.SetEmphasisMark.docx");
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
