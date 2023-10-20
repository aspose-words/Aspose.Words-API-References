---
title: Font.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words für .NET
description: Font Name eigendom. Ruft den Namen der Schriftart ab oder legt diesen fest in C#.
type: docs
weight: 230
url: /de/net/aspose.words/font/name/
---
## Font.Name property

Ruft den Namen der Schriftart ab oder legt diesen fest.

```csharp
public string Name { get; set; }
```

## Bemerkungen

Wenn es kommt, kehrt es zurück[`NameAscii`](../nameascii/).

Beim Einstellen wird eingestellt[`NameAscii`](../nameascii/) ,[`NameBi`](../namebi/) ,[`NameFarEast`](../namefareast/) und[`NameOther`](../nameother/) auf den angegebenen Wert.

## Beispiele

Zeigt, wie eine Textzeile mithilfe ihrer Schriftarteigenschaft formatiert wird.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

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
