---
title: Font.Shadow
second_title: Aspose.Words für .NET-API-Referenz
description: Font eigendom. True wenn die Schriftart als schattiert formatiert ist.
type: docs
weight: 330
url: /de/net/aspose.words/font/shadow/
---
## Font.Shadow property

True, wenn die Schriftart als schattiert formatiert ist.

```csharp
public bool Shadow { get; set; }
```

### Beispiele

Zeigt, wie man einen mit einem Schatten formatierten Textlauf erstellt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Setzen Sie das Shadow-Flag, um einen versetzten Schatteneffekt anzuwenden.
// es so aussehen lassen, als würden die Buchstaben über der Seite schweben.
builder.Font.Shadow = true;
builder.Font.Size = 36;

builder.Writeln("This text has a shadow.");

doc.Save(ArtifactsDir + "Font.Shadow.docx");
```

### Siehe auch

* class [Font](../)
* namensraum [Aspose.Words](../../font/)
* Montage [Aspose.Words](../../../)


