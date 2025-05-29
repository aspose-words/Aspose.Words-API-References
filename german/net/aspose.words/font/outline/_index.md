---
title: Font.Outline
linktitle: Outline
articleTitle: Outline
second_title: Aspose.Words für .NET
description: Entdecken Sie die Schriftkontur-Funktion. Formatieren Sie Schriften ganz einfach als Konturen für ein einzigartiges Design. Verbessern Sie Ihre Typografie mit dieser einfachen Funktion!
type: docs
weight: 300
url: /de/net/aspose.words/font/outline/
---
## Font.Outline property

Wahr, wenn die Schriftart als Umriss formatiert ist.

```csharp
public bool Outline { get; set; }
```

## Beispiele

Zeigt, wie ein als Gliederung formatierter Textlauf erstellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Setzen Sie das Outline-Flag, um die Füllfarbe des Textes auf Weiß zu ändern und
    // Lassen Sie um jedes Zeichen einen dünnen Umriss in der Originalfarbe des Textes.
builder.Font.Outline = true;
builder.Font.Color = Color.Blue;
builder.Font.Size = 36;

builder.Writeln("This text has an outline.");

doc.Save(ArtifactsDir + "Font.Outline.docx");
```

### Siehe auch

* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
