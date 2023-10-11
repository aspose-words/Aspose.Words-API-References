---
title: Font.EmphasisMark
second_title: Aspose.Words für .NET-API-Referenz
description: Font eigendom. Ruft die auf diese Formatierung angewendete Hervorhebungsmarkierung ab oder legt diese fest.
type: docs
weight: 110
url: /de/net/aspose.words/font/emphasismark/
---
## Font.EmphasisMark property

Ruft die auf diese Formatierung angewendete Hervorhebungsmarkierung ab oder legt diese fest.

```csharp
public EmphasisMark EmphasisMark { get; set; }
```

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

* enum [EmphasisMark](../../emphasismark/)
* class [Font](../)
* namensraum [Aspose.Words](../../font/)
* Montage [Aspose.Words](../../../)


