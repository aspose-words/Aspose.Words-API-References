---
title: Font.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „Schriftname“, um Ihre Schriftarten einfach anzupassen und festzulegen und so die Attraktivität und Lesbarkeit Ihres Designs zu verbessern.
type: docs
weight: 230
url: /de/net/aspose.words/font/name/
---
## Font.Name property

Ruft den Namen der Schriftart ab oder legt ihn fest.

```csharp
public string Name { get; set; }
```

## Bemerkungen

Beim Erhalten, kehrt zurück[`NameAscii`](../nameascii/).

Beim Einstellen setzt[`NameAscii`](../nameascii/) ,[`NameBi`](../namebi/) ,[`NameFarEast`](../namefareast/) und[`NameOther`](../nameother/) auf den angegebenen Wert.

## Beispiele

Zeigt, wie ein Textlauf mithilfe seiner Schriftarteigenschaft formatiert wird.

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

// Geben Sie die Schriftformatierung an und fügen Sie dann Text hinzu.
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
