---
title: SaveOptions.PrettyFormat
linktitle: PrettyFormat
articleTitle: PrettyFormat
second_title: .NET için Aspose.Words
description: Çıktınızı SaveOptions' PrettyFormat özelliğiyle geliştirin. Daha temiz, iyi yapılandırılmış sonuçlar için etkinleştirin. Varsayılan değer false'tur. Farkı keşfedin!
type: docs
weight: 110
url: /tr/net/aspose.words.saving/saveoptions/prettyformat/
---
## SaveOptions.PrettyFormat property

Ne zaman`doğru` , uygun olduğu durumlarda çıktıyı güzel biçimlerde biçimlendirir. Varsayılan değer`YANLIŞ` .

```csharp
public bool PrettyFormat { get; set; }
```

## Notlar

Ayarla`doğru` HTML, MHTML, EPUB, WordML, RTF, DOCX ve ODT çıktılarını insan tarafından okunabilir hale getirmek için kullanılır. Test veya hata ayıklama için kullanışlıdır.

## Örnekler

Kaydedilmiş bir .html belgesinin ham kodunun okunabilirliğinin nasıl artırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

HtmlSaveOptions htmlOptions = new HtmlSaveOptions(SaveFormat.Html) { PrettyFormat = usePrettyFormat };

doc.Save(ArtifactsDir + "HtmlSaveOptions.PrettyFormat.html", htmlOptions);

// Güzel biçimi etkinleştirmek, sekme durağı ve yeni satır karakterleri ekleyerek ham HTML kodunu daha okunabilir hale getirir.
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

### Ayrıca bakınız

* class [SaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
