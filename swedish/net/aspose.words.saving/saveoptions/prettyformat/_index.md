---
title: SaveOptions.PrettyFormat
linktitle: PrettyFormat
articleTitle: PrettyFormat
second_title: Aspose.Words för .NET
description: Förbättra dina resultat med SaveOptions egenskap PrettyFormat. Aktivera för renare och mer strukturerade resultat. Standardvärdet är falskt. Upptäck skillnaden!
type: docs
weight: 110
url: /sv/net/aspose.words.saving/saveoptions/prettyformat/
---
## SaveOptions.PrettyFormat property

När`sann` , pretty formats output där det är tillämpligt. Standardvärdet är`falsk` .

```csharp
public bool PrettyFormat { get; set; }
```

## Anmärkningar

Ställ in på`sann` för att göra HTML-, MHTML-, EPUB-, WordML-, RTF-, DOCX- och ODT-utdata läsbar för människor. Användbart för testning eller felsökning.

## Exempel

Visar hur man förbättrar läsbarheten hos råkoden i ett sparat .html-dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

HtmlSaveOptions htmlOptions = new HtmlSaveOptions(SaveFormat.Html) { PrettyFormat = usePrettyFormat };

doc.Save(ArtifactsDir + "HtmlSaveOptions.PrettyFormat.html", htmlOptions);

// Aktivering av pretty format gör den råa HTML-koden mer läsbar genom att lägga till tabbstopp och tecken för nya rader.
string html = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.PrettyFormat.html");
string newLine = Environment.NewLine;

if (usePrettyFormat)
    Assert.AreEqual(
        $"<html>{newLine}" +
                    $"\t<head>{newLine}" +
                        $"\t\t<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\" />{newLine}" +
                        $"\t\t<meta http-equiv=\"Content-Style-Type\" content=\"text/css\" />{newLine}" +
                        $"\t\t<meta name=\"generator\" content=\"{BuildVersionInfo.Product} {BuildVersionInfo.Version}\" />{newLine}" +
                        $"\t\t<title>{newLine}" +
                        $"\t\t</title>{newLine}" +
                    $"\t</head>{newLine}" +
                    $"\t<body style=\"font-family:'Times New Roman'; font-size:12pt\">{newLine}" +
                        $"\t\t<div>{newLine}" +
                            $"\t\t\t<p style=\"margin-top:0pt; margin-bottom:0pt\">{newLine}" +
                                $"\t\t\t\t<span>Hello world!</span>{newLine}" +
                            $"\t\t\t</p>{newLine}" +
                            $"\t\t\t<p style=\"margin-top:0pt; margin-bottom:0pt\">{newLine}" +
                                $"\t\t\t\t<span style=\"-aw-import:ignore\">&#xa0;</span>{newLine}" +
                            $"\t\t\t</p>{newLine}" +
                        $"\t\t</div>{newLine}" +
                    $"\t</body>{newLine}</html>", 
        html);
else
    Assert.AreEqual(
        "<html><head><meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\" />" +
                "<meta http-equiv=\"Content-Style-Type\" content=\"text/css\" />" +
                $"<meta name=\"generator\" content=\"{BuildVersionInfo.Product} {BuildVersionInfo.Version}\" /><title></title></head>" +
                "<body style=\"font-family:'Times New Roman'; font-size:12pt\">" +
                "<div><p style=\"margin-top:0pt; margin-bottom:0pt\"><span>Hello world!</span></p>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt\"><span style=\"-aw-import:ignore\">&#xa0;</span></p></div></body></html>", 
        html);
```

### Se även

* class [SaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
