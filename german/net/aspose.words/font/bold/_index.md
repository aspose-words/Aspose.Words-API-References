---
title: Font.Bold
linktitle: Bold
articleTitle: Bold
second_title: Aspose.Words für .NET
description: Font Bold eigendom. True wenn die Schriftart fett formatiert ist in C#.
type: docs
weight: 40
url: /de/net/aspose.words/font/bold/
---
## Font.Bold property

True, wenn die Schriftart fett formatiert ist.

```csharp
public bool Bold { get; set; }
```

## Beispiele

Zeigt, wie formatierter Text mit DocumentBuilder eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Geben Sie die Schriftartformatierung an und fügen Sie dann Text hinzu.
Aspose.Words.Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Courier New";
font.Underline = Underline.Dash;

builder.Write("Hello world!");
```

### Siehe auch

* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
