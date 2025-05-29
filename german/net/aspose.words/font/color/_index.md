---
title: Font.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words für .NET
description: Entdecken Sie die Schriftfarben-Eigenschaft, um die Textfarben in Ihren Designs einfach anzupassen. Verbessern Sie Lesbarkeit und Ästhetik mit lebendigen, auffälligen Farbtönen!
type: docs
weight: 70
url: /de/net/aspose.words/font/color/
---
## Font.Color property

Ruft die Farbe der Schriftart ab oder legt sie fest.

```csharp
public Color Color { get; set; }
```

## Beispiele

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

Zeigt, wie ein Hyperlink-Feld eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// Fügen Sie einen Hyperlink ein und heben Sie ihn mit benutzerdefinierter Formatierung hervor.
// Der Hyperlink ist ein anklickbarer Text, der uns zum in der URL angegebenen Ort führt.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", false);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Strg + Linksklick auf den Link im Text in Microsoft Word führt uns über ein neues Webbrowserfenster zur URL.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

### Siehe auch

* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
