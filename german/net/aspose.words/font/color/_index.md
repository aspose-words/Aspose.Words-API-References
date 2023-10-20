---
title: Font.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words für .NET
description: Font Color eigendom. Ruft die Farbe der Schriftart ab oder legt sie fest in C#.
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

// Geben Sie die Schriftartformatierung an und fügen Sie dann Text hinzu.
Aspose.Words.Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Courier New";
font.Underline = Underline.Dash;

builder.Write("Hello world!");
```

Zeigt, wie ein Hyperlinkfeld eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// Einen Hyperlink einfügen und ihn mit benutzerdefinierter Formatierung hervorheben.
// Der Hyperlink ist ein anklickbarer Text, der uns zu dem in der URL angegebenen Ort führt.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", false);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Strg + Linksklick auf den Link im Text in Microsoft Word führt uns über ein neues Webbrowser-Fenster zur URL.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

### Siehe auch

* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
