---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportRelativeFontSize yöntemi"
linktitle: "get_ExportRelativeFontSize"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportRelativeFontSize yöntemi. HTML, MHTML veya EPUB olarak kaydederken yazı tipi boyutlarının göreceli birimlerde çıktılanıp çıktılanmayacağını belirtir. Varsayılan değer C++'ta false'tur."
type: docs
weight: 25000
url: /tr/cpp/aspose.words.saving/htmlsaveoptions/get_exportrelativefontsize/
---
## HtmlSaveOptions::get_ExportRelativeFontSize method


HTML, MHTML veya EPUB olarak kaydederken yazı tipi boyutlarının göreceli birimlerde çıktılanıp çıktılanmayacağını belirtir. Varsayılan değer **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportRelativeFontSize() const
```

## Açıklamalar


Birçok mevcut belgede (HTML, IDPF EPUB) yazı tipi boyutları göreceli birimlerle belirtilir. Bu, uygulamaların belgeleri görüntülerken/işlerken metin boyutunu ayarlamasına olanak tanır. Örneğin, Microsoft Internet Explorer'ın "View->Text Size" alt menüsü, Adobe Digital Editions'ın iki düğmesi vardır: Increase/Decrease Text Size. Bu işlevin çalışmasını bekliyorsanız [ExportRelativeFontSize](./) özelliğini **true** olarak ayarlayın.

**Aspose**[Words](../../../aspose.words/) document model contains and operates only with absolute font size units. Relative units need additional logic to be recalculated from some initial (standard) size. [Font](../../../aspose.words/font/) size of **Normal** document style is taken as standard. For instance, if **Normal** has 12pt font and some text is 18pt then it will be output as **%1.5em.** to the HTML.

Bu seçenek etkinleştirildiğinde, metin dışındaki belge öğeleri hâlâ mutlak boyutlara sahip olur. Ayrıca bazı metinle ilgili nitelikler mutlak olarak ifade edilebilir. Özellikle, "exactly" kuralı ile belirtilen satır aralığı, metin ölçeklendirilirken istenmeyen sonuçlar doğurabilir. Bu nedenle, [ExportRelativeFontSize](./) **true** olarak ayarlandığında dışa aktarma yapılmadan önce kaynak belgeler düzgün bir şekilde tasarlanmalı ve test edilmelidir.

## Örnekler



.html olarak kaydederken göreceli yazı tipi boyutlarının nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Default font size, ");
builder->get_Font()->set_Size(24);
builder->Writeln(u"2x default font size,");
builder->get_Font()->set_Size(96);
builder->Write(u"8x default font size");

// Belgeyi HTML olarak kaydettiğimizde, bir SaveOptions nesnesi geçebiliriz.
// göreceli mi yoksa mutlak mı yazı tipi boyutları kullanılacağını belirlemek için.
// "ExportRelativeFontSize" bayrağını "true" olarak ayarlayarak yazı tipi boyutlarını belirtin
// "em" ölçü birimini kullanarak, bu birim mevcut yazı tipi boyutunu çarpan bir faktördür.
// "ExportRelativeFontSize" bayrağını "false" olarak ayarlayarak yazı tipi boyutlarını belirtin
// "pt" ölçü birimini kullanarak, bu birim yazı tipinin nokta cinsinden mutlak boyutudur.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportRelativeFontSize(exportRelativeFontSize);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.RelativeFontSize.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.RelativeFontSize.html");

if (exportRelativeFontSize)
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<body style=\"font-family:'Times New Roman'\">") + u"<div>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt\">" + u"<span>Default font size, </span>" + u"</p>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:2em\">" + u"<span>2x default font size,</span>" + u"</p>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:8em\">" + u"<span>8x default font size</span>" + u"</p>" + u"</div>" + u"</body>"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<body style=\"font-family:'Times New Roman'; font-size:12pt\">") + u"<div>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt\">" + u"<span>Default font size, </span>" + u"</p>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:24pt\">" + u"<span>2x default font size,</span>" + u"</p>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:96pt\">" + u"<span>8x default font size</span>" + u"</p>" + u"</div>" + u"</body>"));
}
```

## Ayrıca Bakınız

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
