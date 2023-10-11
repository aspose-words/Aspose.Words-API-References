---
title: SaveOptions.PrettyFormat
second_title: Aspose.Words für .NET-API-Referenz
description: SaveOptions eigendom. WannWAHR hübsche Ausgabeformate sofern zutreffend. Der Standardwert istFALSCH .
type: docs
weight: 110
url: /de/net/aspose.words.saving/saveoptions/prettyformat/
---
## SaveOptions.PrettyFormat property

Wann`WAHR` hübsche Ausgabeformate, sofern zutreffend. Der Standardwert ist`FALSCH` .

```csharp
public bool PrettyFormat { get; set; }
```

### Bemerkungen

Einstellen`WAHR` um HTML-, MHTML-, EPUB-, WordML-, RTF-, DOCX- und ODT-Ausgaben für Menschen lesbar zu machen. Nützlich zum Testen oder Debuggen.

### Beispiele

Zeigt, wie die Lesbarkeit des Rohcodes eines gespeicherten HTML-Dokuments verbessert werden kann.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

HtmlSaveOptions htmlOptions = new HtmlSaveOptions(SaveFormat.Html) { PrettyFormat = usePrettyFormat };

doc.Save(ArtifactsDir + "HtmlSaveOptions.PrettyFormat.html", htmlOptions);

// Durch die Aktivierung des hübschen Formats wird der rohe HTML-Code durch Hinzufügen von Tabstopp- und Zeilenumbruchzeichen besser lesbar.
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

### Siehe auch

* class [SaveOptions](../)
* namensraum [Aspose.Words.Saving](../../saveoptions/)
* Montage [Aspose.Words](../../../)


