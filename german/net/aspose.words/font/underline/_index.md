---
title: Font.Underline
second_title: Aspose.Words für .NET-API-Referenz
description: Font eigendom. Ruft den Typ der auf die Schriftart angewendeten Unterstreichung ab oder legt diesen fest.
type: docs
weight: 530
url: /de/net/aspose.words/font/underline/
---
## Font.Underline property

Ruft den Typ der auf die Schriftart angewendeten Unterstreichung ab oder legt diesen fest.

```csharp
public Underline Underline { get; set; }
```

### Beispiele

Zeigt, wie Sie den Stil und die Farbe einer Textunterstreichung konfigurieren.

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

* enum [Underline](../../underline/)
* class [Font](../)
* namensraum [Aspose.Words](../../font/)
* Montage [Aspose.Words](../../../)


