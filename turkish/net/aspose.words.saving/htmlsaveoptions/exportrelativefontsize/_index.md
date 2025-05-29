---
title: HtmlSaveOptions.ExportRelativeFontSize
linktitle: ExportRelativeFontSize
articleTitle: ExportRelativeFontSize
second_title: .NET için Aspose.Words
description: HTML, MHTML veya EPUB formatlarında yazı tipi boyutlarını özelleştirmek için HtmlSaveOptions ExportRelativeFontSize özelliğini keşfedin. Okunabilirliği kolaylıkla artırın!
type: docs
weight: 230
url: /tr/net/aspose.words.saving/htmlsaveoptions/exportrelativefontsize/
---
## HtmlSaveOptions.ExportRelativeFontSize property

HTML, MHTML veya EPUB'a kaydederken yazı tipi boyutlarının göreli birimlerde çıktı verilip verilmeyeceğini belirtir. Varsayılan`YANLIŞ` .

```csharp
public bool ExportRelativeFontSize { get; set; }
```

## Notlar

Birçok mevcut belgede (HTML, IDPF EPUB) yazı tipi boyutları göreceli birimlerle belirtilir. Bu, uygulamaların belgeleri görüntülerken/işlerken metin boyutunu ayarlamasına olanak tanır. Örneğin, Microsoft Internet Explorer "Görünüm-&gt;Metin Boyutu" alt menüsüne sahiptir, Adobe Digital Editions'ın iki düğmesi vardır: Metin Boyutunu Artır/Azalt. Bu işlevselliğin çalışmasını bekliyorsanız,`ExportRelativeFontSize` mülk`doğru` .

Aspose Words belge modeli yalnızca mutlak yazı tipi boyutu birimlerini içerir ve bunlarla çalışır. Göreceli birimler, bazı başlangıç (standart) boyutlarından yeniden hesaplanmak üzere ek mantığına ihtiyaç duyar. Yazı tipi boyutu**Normal** belge style standart olarak alınır. Örneğin, eğer**Normal** 12pt yazı tipi ve bazı metinler 18pt ise çıktı şu şekilde olacaktır**1,5 cm.** HTML'ye.

Bu seçenek etkinleştirildiğinde, metin dışındaki belge öğeleri hala mutlak boyutlara sahip olacaktır. Ayrıca, bazı metinle ilgili öznitelikler mutlak olarak ifade edilebilir. Özellikle, "exactly" rule ile belirtilen satır aralığı, metin ölçeklenirken istenmeyen sonuçlar üretebilir. Bu nedenle kaynak belgeler, dışa aktarılırken düzgün bir şekilde tasarlanmalı ve test edilmelidir `ExportRelativeFontSize` ayarlandı`doğru`.

## Örnekler

.html'e kaydederken göreceli yazı tipi boyutlarının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Default font size, ");
builder.Font.Size = 24;
builder.Writeln("2x default font size,");
builder.Font.Size = 96;
builder.Write("8x default font size");

// Belgeyi HTML'e kaydettiğimizde, SaveOptions nesnesini geçirebiliriz
// bağıl veya mutlak yazı tipi boyutlarının kullanılıp kullanılmayacağını belirlemek için.
// Yazı tipi boyutlarını belirtmek için "ExportRelativeFontSize" bayrağını "true" olarak ayarlayın
 // geçerli yazı tipi boyutunu çarpan bir faktör olan "em" ölçüm birimini kullanarak.
// Yazı tipi boyutlarını bildirmek için "ExportRelativeFontSize" bayrağını "false" olarak ayarlayın
// yazı tipinin nokta cinsinden mutlak boyutunu ifade eden "pt" ölçüm birimini kullanarak.
HtmlSaveOptions options = new HtmlSaveOptions { ExportRelativeFontSize = exportRelativeFontSize };

doc.Save(ArtifactsDir + "HtmlSaveOptions.RelativeFontSize.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.RelativeFontSize.html");

if (exportRelativeFontSize)
{
    Assert.True(outDocContents.Contains(
        "<body style=\"font-family:'Times New Roman'\">" +
            "<div>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                    "<span>Default font size, </span>" +
                "</p>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:2em\">" +
                    "<span>2x default font size,</span>" +
                "</p>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:8em\">" +
                    "<span>8x default font size</span>" +
                "</p>" +
            "</div>" +
        "</body>"));
}
else
{
    Assert.True(outDocContents.Contains(
        "<body style=\"font-family:'Times New Roman'; font-size:12pt\">" +
            "<div>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                    "<span>Default font size, </span>" +
                "</p>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:24pt\">" +
                    "<span>2x default font size,</span>" +
                "</p>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:96pt\">" +
                    "<span>8x default font size</span>" +
                "</p>" +
            "</div>" +
        "</body>"));
}
```

### Ayrıca bakınız

* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
