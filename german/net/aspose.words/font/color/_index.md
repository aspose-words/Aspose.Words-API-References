---
title: Font.Color
second_title: Aspose.Words für .NET-API-Referenz
description: Font eigendom. Ruft die Farbe der Schriftart ab oder legt sie fest.
type: docs
weight: 70
url: /de/net/aspose.words/font/color/
---
## Font.Color property

Ruft die Farbe der Schriftart ab oder legt sie fest.

```csharp
public Color Color { get; set; }
```

### Beispiele

Zeigt, wie formatierter Text mit DocumentBuilder eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Schriftartformatierung angeben, dann Text hinzufügen.
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

// Hyperlink einfügen und mit benutzerdefinierter Formatierung hervorheben.
// Der Hyperlink ist ein anklickbares Textstück, das uns zu der in der URL angegebenen Stelle führt.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", falsch);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Strg + Linksklick auf den Link im Text in Microsoft Word bringt uns über ein neues Webbrowser-Fenster zur URL.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

### Siehe auch

* class [Font](../)
* namensraum [Aspose.Words](../../font/)
* Montage [Aspose.Words](../../../)


