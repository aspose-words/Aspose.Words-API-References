---
title: Font.EmphasisMark
linktitle: EmphasisMark
articleTitle: EmphasisMark
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie mit der Schriftart-Hervorhebungseigenschaft Ihre Textformatierung verbessern. Erfahren Sie, wie Sie Hervorhebungen für eine bessere Lesbarkeit festlegen und anpassen.
type: docs
weight: 110
url: /de/net/aspose.words/font/emphasismark/
---
## Font.EmphasisMark property

Ruft das Hervorhebungszeichen ab oder legt es fest, das auf diese Formatierung angewendet wird.

```csharp
public EmphasisMark EmphasisMark { get; set; }
```

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

* enum [EmphasisMark](../../emphasismark/)
* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
