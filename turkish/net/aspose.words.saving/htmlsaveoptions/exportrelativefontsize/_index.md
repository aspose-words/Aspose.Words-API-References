---
title: HtmlSaveOptions.ExportRelativeFontSize
second_title: Aspose.Words for .NET API Referansı
description: HtmlSaveOptions mülk. HTML MHTML veya EPUBa kaydederken yazı tipi boyutlarının göreli birimler halinde çıkarılıp çıkarılmayacağını belirtir. VarsayılanYANLIŞ .
type: docs
weight: 230
url: /tr/net/aspose.words.saving/htmlsaveoptions/exportrelativefontsize/
---
## HtmlSaveOptions.ExportRelativeFontSize property

HTML, MHTML veya EPUB'a kaydederken yazı tipi boyutlarının göreli birimler halinde çıkarılıp çıkarılmayacağını belirtir. Varsayılan:`YANLIŞ` .

```csharp
public bool ExportRelativeFontSize { get; set; }
```

### Notlar

Mevcut birçok belgede (HTML, IDPF EPUB) yazı tipi boyutları göreceli birimlerle belirtilir. Bu, uygulamalarının belgeleri görüntülerken/işlerken metin boyutunu ayarlamasına olanak tanır. Örneğin, Microsoft Internet Explorer 'nin "Görünüm-&gt;Metin Boyutu" alt menüsü vardır, Adobe Digital Editions'ın iki düğmesi vardır: Metin Boyutunu Artır/Azalt. Bu işlevin çalışmasını bekliyorsanız o zaman ayarlayın`ExportRelativeFontSize` mülkiyet`doğru` .

Aspose Words belge modeli yalnızca mutlak yazı tipi boyutu birimlerini içerir ve bunlarla çalışır. Göreli birimlerin bazı başlangıç (standart) boyutlardan yeniden hesaplanması için ek mantığa ihtiyacı vardır. Yazı tipi boyutu **Normal** belge stili standart olarak alınır. Örneğin, eğer **Normal** 12 puntoluk yazı tipi varsa ve bazı metinler 18 punto ise, olarak çıkarılacaktır. **1.5em.** HTML'ye.

Bu seçenek etkinleştirildiğinde, metin dışındaki belge öğeleri hâlâ mutlak boyutlara sahip olacaktır. Ayrıca metinle ilgili bazı nitelikler mutlak olarak ifade edilebilir. Özellikle, "tam olarak" kuralı ile belirtilen satır aralığı, metni ölçeklendirirken istenmeyen sonuçlar doğurabilir. Bu nedenle, kaynak belgeler dışa aktarılırken doğru şekilde tasarlanmalı ve test edilmelidir.`ExportRelativeFontSize` ayarlanır`doğru`.

### Örnekler

.html'ye kaydederken göreli yazı tipi boyutlarının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Default font size, ");
builder.Font.Size = 24;
builder.Writeln("2x default font size,");
builder.Font.Size = 96;
builder.Write("8x default font size");

// Belgeyi HTML'ye kaydettiğimizde SaveOptions nesnesini iletebiliriz
// göreli veya mutlak yazı tipi boyutlarının kullanılıp kullanılmayacağını belirlemek için.
// Yazı tipi boyutlarını bildirmek için "ExportRelativeFontSize" bayrağını "true" olarak ayarlayın
 // mevcut yazı tipi boyutunu çarpan bir faktör olan "em" ölçü birimini kullanarak.
// Yazı tipi boyutlarını bildirmek için "ExportRelativeFontSize" bayrağını "false" olarak ayarlayın
// yazı tipinin nokta cinsinden mutlak boyutu olan "pt" ölçü birimini kullanarak.
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
* ad alanı [Aspose.Words.Saving](../../htmlsaveoptions/)
* toplantı [Aspose.Words](../../../)


