---
title: SaveOptions.PrettyFormat
linktitle: PrettyFormat
articleTitle: PrettyFormat
second_title: Aspose.Words pour .NET
description: Améliorez vos résultats grâce à la propriété PrettyFormat de SaveOptions. Activez-la pour des résultats plus clairs et bien structurés. La valeur par défaut est « false ». Découvrez la différence !
type: docs
weight: 110
url: /fr/net/aspose.words.saving/saveoptions/prettyformat/
---
## SaveOptions.PrettyFormat property

Quand`vrai` , joli format de sortie le cas échéant. La valeur par défaut est`FAUX` .

```csharp
public bool PrettyFormat { get; set; }
```

## Remarques

Régler sur`vrai` pour rendre les sorties HTML, MHTML, EPUB, WordML, RTF, DOCX et ODT lisibles par l'homme. Utile pour les tests ou le débogage.

## Exemples

Montre comment améliorer la lisibilité du code brut d'un document .html enregistré.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

HtmlSaveOptions htmlOptions = new HtmlSaveOptions(SaveFormat.Html) { PrettyFormat = usePrettyFormat };

doc.Save(ArtifactsDir + "HtmlSaveOptions.PrettyFormat.html", htmlOptions);

// L'activation du joli format rend le code HTML brut plus lisible en ajoutant des caractères de tabulation et de nouvelle ligne.
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

### Voir également

* class [SaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
