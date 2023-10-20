---
title: Font.Engrave
linktitle: Engrave
articleTitle: Engrave
second_title: Aspose.Words für .NET
description: Font Engrave eigendom. True wenn die Schriftart als graviert formatiert ist in C#.
type: docs
weight: 120
url: /de/net/aspose.words/font/engrave/
---
## Font.Engrave property

True, wenn die Schriftart als graviert formatiert ist.

```csharp
public bool Engrave { get; set; }
```

## Beispiele

Zeigt, wie Gravur-/Prägeeffekte auf Text angewendet werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.Color = Color.LightBlue;

// Nachfolgend finden Sie zwei Möglichkeiten, Schatten zu verwenden, um dem Text einen 3D-ähnlichen Effekt zu verleihen.
// 1 – Text so eingravieren, dass es aussieht, als wären die Buchstaben in die Seite eingelassen:
builder.Font.Engrave = true;

builder.Writeln("This text is engraved.");

// 2 – Prägen Sie den Text so ein, dass er aussieht, als würden die Buchstaben aus der Seite herausspringen:
builder.Font.Engrave = false;
builder.Font.Emboss = true;

builder.Writeln("This text is embossed.");

doc.Save(ArtifactsDir + "Font.EngraveEmboss.docx");
```

### Siehe auch

* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
