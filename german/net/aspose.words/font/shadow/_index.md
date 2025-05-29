---
title: Font.Shadow
linktitle: Shadow
articleTitle: Shadow
second_title: Aspose.Words für .NET
description: Entdecken Sie die Font Shadow-Eigenschaft und verbessern Sie Ihren Text mit stilvollen Schatteneffekten für eine beeindruckende visuelle Wirkung Ihrer Designs.
type: docs
weight: 340
url: /de/net/aspose.words/font/shadow/
---
## Font.Shadow property

Wahr, wenn die Schriftart als schattiert formatiert ist.

```csharp
public bool Shadow { get; set; }
```

## Beispiele

Zeigt, wie ein mit Schatten formatierter Textlauf erstellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Setzen Sie das Schatten-Flag, um einen versetzten Schatteneffekt anzuwenden.
// sodass es so aussieht, als würden die Buchstaben über der Seite schweben.
builder.Font.Shadow = true;
builder.Font.Size = 36;

builder.Writeln("This text has a shadow.");

doc.Save(ArtifactsDir + "Font.Shadow.docx");
```

### Siehe auch

* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
