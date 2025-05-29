---
title: Font.Underline
linktitle: Underline
articleTitle: Underline
second_title: Aspose.Words für .NET
description: Entdecken Sie die Funktion „Schriftunterstreichung“, um Textstile anzupassen. Legen Sie Unterstreichungsarten einfach fest und ändern Sie sie für eine verbesserte Typografie in Ihren Designs.
type: docs
weight: 540
url: /de/net/aspose.words/font/underline/
---
## Font.Underline property

Ruft den Unterstreichungstyp der Schriftart ab oder legt ihn fest.

```csharp
public Underline Underline { get; set; }
```

## Beispiele

Zeigt, wie Sie Stil und Farbe einer Textunterstreichung konfigurieren.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Underline = Underline.Dotted;
builder.Font.UnderlineColor = Color.Red;

builder.Writeln("Underlined text.");

doc.Save(ArtifactsDir + "Font.Underlines.docx");
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

* enum [Underline](../../underline/)
* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
