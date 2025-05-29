---
title: Font.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words för .NET
description: Återställ din text till dess ursprungliga stil med Font ClearFormatting-metoden. Njut av ren och konsekvent formatering för ett polerat utseende!
type: docs
weight: 560
url: /sv/net/aspose.words/font/clearformatting/
---
## Font.ClearFormatting method

Återställer till standardtypsnittsformatering.

```csharp
public void ClearFormatting()
```

## Anmärkningar

Tar bort all teckensnittsformatering som explicit anges på objektet från vilket [`Font`](../) erhölls så teckensnittsformateringen kommer att ärvas från , lämplig förälder.

## Exempel

Visar hur man infogar ett hyperlänkfält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// Infoga en hyperlänk och framhäv den med anpassad formatering.
// Hyperlänken kommer att vara en klickbar textbit som tar oss till den plats som anges i URL:en.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", falskt);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Ctrl + vänsterklicka på länken i texten i Microsoft Word tar oss till URL:en via ett nytt webbläsarfönster.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

### Se även

* class [Font](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
