---
title: Enum EmphasisMark
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.EmphasisMark opsomming. Gibt mögliche Arten von Hervorhebungsmarkierungen an.
type: docs
weight: 1460
url: /de/net/aspose.words/emphasismark/
---
## EmphasisMark enumeration

Gibt mögliche Arten von Hervorhebungsmarkierungen an.

```csharp
public enum EmphasisMark
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Keine Hervorhebungsmarkierung. |
| OverSolidCircle | `1` | Hervorhebungszeichen ist ein durchgehender schwarzer Kreis, der über dem Text angezeigt wird. |
| OverComma | `2` | Hervorhebungszeichen ist ein Kommazeichen, das über dem Text angezeigt wird. |
| OverWhiteCircle | `3` | Hervorhebungszeichen ist ein leerer weißer Kreis, der über dem Text angezeigt wird. |
| UnderSolidCircle | `4` | Hervorhebungszeichen ist ein durchgehender schwarzer Kreis, der unter dem Text angezeigt wird. |

### Beispiele

Zeigt, wie man zusätzliche Zeichen hinzufügt, die über/unter dem Glyphenzeichen gerendert werden.

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


