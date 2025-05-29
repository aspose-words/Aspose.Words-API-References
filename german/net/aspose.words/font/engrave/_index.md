---
title: Font.Engrave
linktitle: Engrave
articleTitle: Engrave
second_title: Aspose.Words für .NET
description: Entdecken Sie die Funktion „Font Engrave“. Formatieren Sie Schriftarten ganz einfach für einen eleganten Gravur-Look und steigern Sie so die Raffinesse und Attraktivität Ihres Designs.
type: docs
weight: 120
url: /de/net/aspose.words/font/engrave/
---
## Font.Engrave property

Wahr, wenn die Schriftart als graviert formatiert ist.

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

// Unten sind zwei Möglichkeiten aufgeführt, wie Sie mit Schatten dem Text einen 3D-ähnlichen Effekt verleihen können.
// 1 - Gravieren Sie den Text, sodass es aussieht, als wären die Buchstaben in die Seite vertieft:
builder.Font.Engrave = true;

builder.Writeln("This text is engraved.");

// 2 - Prägen Sie den Text, damit es aussieht, als würden die Buchstaben aus der Seite herausspringen:
builder.Font.Engrave = false;
builder.Font.Emboss = true;

builder.Writeln("This text is embossed.");

doc.Save(ArtifactsDir + "Font.EngraveEmboss.docx");
```

### Siehe auch

* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
