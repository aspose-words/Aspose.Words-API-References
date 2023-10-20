---
title: Font.Italic
linktitle: Italic
articleTitle: Italic
second_title: Aspose.Words für .NET
description: Font Italic eigendom. True wenn die Schriftart kursiv formatiert ist in C#.
type: docs
weight: 160
url: /de/net/aspose.words/font/italic/
---
## Font.Italic property

True, wenn die Schriftart kursiv formatiert ist.

```csharp
public bool Italic { get; set; }
```

## Beispiele

Zeigt, wie man mit einem Document Builder kursiven Text schreibt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.Italic = true;
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "Font.Italic.docx");
```

### Siehe auch

* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
