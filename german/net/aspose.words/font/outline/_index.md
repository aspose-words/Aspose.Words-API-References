---
title: Font.Outline
second_title: Aspose.Words für .NET-API-Referenz
description: Font eigendom. True wenn die Schriftart als Outline formatiert ist.
type: docs
weight: 290
url: /de/net/aspose.words/font/outline/
---
## Font.Outline property

True, wenn die Schriftart als Outline formatiert ist.

```csharp
public bool Outline { get; set; }
```

### Beispiele

Zeigt, wie man einen als Gliederung formatierten Textlauf erstellt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Setzen Sie das Outline-Flag, um die Füllfarbe des Texts in Weiß zu ändern
 // Lassen Sie um jedes Zeichen einen dünnen Umriss in der Originalfarbe des Textes.
builder.Font.Outline = true;
builder.Font.Color = Color.Blue;
builder.Font.Size = 36;

builder.Writeln("This text has an outline.");

doc.Save(ArtifactsDir + "Font.Outline.docx");
```

### Siehe auch

* class [Font](../)
* namensraum [Aspose.Words](../../font/)
* Montage [Aspose.Words](../../../)


