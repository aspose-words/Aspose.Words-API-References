---
title: SaveOptions.PrettyFormat
linktitle: PrettyFormat
articleTitle: PrettyFormat
second_title: Aspose.Words pour .NET
description: SaveOptions PrettyFormat propriété. Quandvrai jolis formats de sortie le cas échéant. La valeur par défaut estFAUX  en C#.
type: docs
weight: 110
url: /fr/net/aspose.words.saving/saveoptions/prettyformat/
---
## SaveOptions.PrettyFormat property

Quand`vrai` jolis formats de sortie le cas échéant. La valeur par défaut est`FAUX` .

```csharp
public bool PrettyFormat { get; set; }
```

## Remarques

Mis à`vrai` pour rendre les sorties HTML, MHTML, EPUB, WordML, RTF, DOCX et ODT lisibles par l'homme. Utile pour les tests ou le débogage.

## Exemples

Montre comment améliorer la lisibilité du code brut d’un document .html enregistré.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

HtmlSaveOptions htmlOptions = new HtmlSaveOptions(SaveFormat.Html) { PrettyFormat = usePrettyFormat };

doc.Save(ArtifactsDir + "HtmlSaveOptions.PrettyFormat.html", htmlOptions);

// L'activation du joli format rend le code HTML brut plus lisible en ajoutant des taquets de tabulation et des caractères de nouvelle ligne.
string html = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.PrettyFormat.html");

if (usePrettyFormat)
    Assert.AreEqual(
        "<html>\r\n" +
                    "\t<head>\r\n" +
                        "\t\t<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\" />\r\n" +
                        "\t\t<meta http-equiv=\"Content-Style-Type\" content=\"text/css\" />\r\n" +
                        $"\t\t<meta name=\"generator\" content=\"{BuildVersionInfo.Product} {BuildVersionInfo.Version}\" />\r\n" +
                        "\t\t<title>\r\n" +
                        "\t\t</title>\r\n" +
                    "\t</head>\r\n" +
                    "\t<body style=\"font-family:'Times New Roman'; font-size:12pt\">\r\n" +
                        "\t\t<div>\r\n" +
                            "\t\t\t<p style=\"margin-top:0pt; margin-bottom:0pt\">\r\n" +
                                "\t\t\t\t<span>Hello world!</span>\r\n" +
                            "\t\t\t</p>\r\n" +
                            "\t\t\t<p style=\"margin-top:0pt; margin-bottom:0pt\">\r\n" +
                                "\t\t\t\t<span style=\"-aw-import:ignore\">&#xa0;</span>\r\n" +
                            "\t\t\t</p>\r\n" +
                        "\t\t</div>\r\n" +
                    "\t</body>\r\n</html>", 
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

### Voir également

* class [SaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
