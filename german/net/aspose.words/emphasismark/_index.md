---
title: Enum EmphasisMark
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.EmphasisMark opsomming. Gibt mögliche Arten von Hervorhebungszeichen an.
type: docs
weight: 1310
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
| OverComma | `2` | Das Hervorhebungszeichen ist ein Kommazeichen, das über dem Text angezeigt wird. |
| OverWhiteCircle | `3` | Das Hervorhebungszeichen ist ein leerer weißer Kreis, der über dem Text angezeigt wird. |
| UnderSolidCircle | `4` | Das Hervorhebungszeichen ist ein ausgefüllter schwarzer Kreis, der unter dem Text angezeigt wird. |

### Beispiele

Zeigt, wie zusätzliche Zeichen hinzugefügt werden, die über/unter dem Glyphenzeichen gerendert werden.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// Mögliche Arten von Hervorhebungen:
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


