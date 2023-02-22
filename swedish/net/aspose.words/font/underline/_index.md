---
title: Font.Underline
second_title: Aspose.Words för .NET API Referens
description: Font fast egendom. Hämtar eller ställer in typen av understrykning som appliceras på teckensnittet.
type: docs
weight: 530
url: /sv/net/aspose.words/font/underline/
---
## Font.Underline property

Hämtar eller ställer in typen av understrykning som appliceras på teckensnittet.

```csharp
public Underline Underline { get; set; }
```

### Exempel

Visar hur du konfigurerar stilen och färgen på en textunderstrykning.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Underline = Underline.Dotted;
builder.Font.UnderlineColor = Color.Red;

builder.Writeln("Underlined text.");

doc.Save(ArtifactsDir + "Font.Underlines.docx");
```

Visar hur man infogar formaterad text med DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ange teckensnittsformatering och lägg sedan till text.
Aspose.Words.Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Courier New";
font.Underline = Underline.Dash;

builder.Write("Hello world!");
```

Visar hur man infogar ett hyperlänkfält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// Infoga en hyperlänk och framhäva den med anpassad formatering.
// Hyperlänken kommer att vara ett klickbart stycke text som tar oss till den plats som anges i URL:en.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", false);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Ctrl + vänsterklicka på länken i texten i Microsoft Word tar oss till URL:en via ett nytt webbläsarfönster.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

### Se även

* enum [Underline](../../underline/)
* class [Font](../)
* namnutrymme [Aspose.Words](../../font/)
* hopsättning [Aspose.Words](../../../)


