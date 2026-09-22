---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold metodu"
linktitle: "get_FontResourcesSubsettingSizeThreshold"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold metodu. HTML, MHTML veya EPUB olarak kaydedilirken hangi yazı tipi kaynaklarının alt kümeleme (subsetting) gerektirdiğini kontrol eder. Varsayılan değer C++'da %0'dır."
type: docs
weight: 31000
url: /tr/cpp/aspose.words.saving/htmlsaveoptions/get_fontresourcessubsettingsizethreshold/
---
## HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold method


HTML, MHTML veya EPUB olarak kaydederken hangi yazı tipi kaynaklarının alt kümelendirilmesi gerektiğini denetler. Varsayılan değer **%0**.

```cpp
int32_t Aspose::Words::Saving::HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold() const
```

## Açıklamalar


[ExportFontResources](../get_exportfontresources/) allows exporting fonts as subsidiary files or as parts of the output package. If the document uses many fonts, especially with large number of glyphs, then output size can grow significantly. [Font](../../../aspose.words/font/) subsetting reduces the size of the exported font resource by filtering out glyphs that are not used by the current document.

[Font](../../../aspose.words/font/) subsetting works as follows:

* By default, all exported fonts are subsetted.
* Setting [FontResourcesSubsettingSizeThreshold](./) to a positive value instructs Aspose.Words to subset fonts which file size is larger than the specified value.
* Setting the property to **MaxValue** suppresses font subsetting.



**Important!** When exporting font resources, font licensing issues should be considered. Authors who want to use specific fonts via a downloadable font mechanism must always carefully verify that their intended use is within the scope of the font license. Many commercial fonts presently do not allow web downloading of their fonts in any form. [License](../../../aspose.words/license/) agreements that cover some fonts specifically note that usage via **%@font-face** rules in CSS style sheets is not allowed. [Font](../../../aspose.words/font/) subsetting can also violate license terms.

## Örnekler



Yazı tipi alt kümeleme ile nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Times New Roman");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Courier New");
builder->Writeln(u"Hello world!");

// Belgeyi HTML olarak kaydettiğimizde, yazı tipi alt kümelemeyi yapılandırmak için bir SaveOptions nesnesi geçirebiliriz.
// "ExportFontResources" bayrağını "true" olarak ayarladığımızı ve ayrıca "FontsFolder" özelliğinde bir klasör adı belirlediğimizi varsayalım.
// Bu durumda, kaydetme işlemi o klasörü oluşturacak ve içine bir .ttf dosyası yerleştirecektir
// belgemizin kullandığı her yazı tipi için o klasöre.
// Her .ttf dosyası, ilgili yazı tipinin tüm glif kümesini içerecektir,
// bu da belgeye eşlik eden çok büyük bir dosyaya yol açabilir.
// Bir yazı tipine alt kümeleme uyguladığımızda, dışa aktarılan ham verisi yalnızca belgenin
// kullandığı glifleri içerir, tüm glif kümesi yerine. Belgemizdeki metin bir yazı tipinin sadece küçük bir kısmını kullanıyorsa
// glif kümesi, alt kümeleme çıktı belgelerimizin boyutunu önemli ölçüde azaltacaktır.
// "FontResourcesSubsettingSizeThreshold" özelliğini .ttf dosya boyutunu bayt cinsinden tanımlamak için kullanabiliriz.
// Eğer dışa aktarılan bir yazı tipi bu değerden daha büyük bir dosya oluşturursa, kaydetme işlemi o yazı tipine alt kümeleme uygular.
// 0 eşik değeri ayarlamak, tüm yazı tiplerine alt kümeleme uygular,
// ve "int.MaxValue" olarak ayarlamak, alt kümelemeyi etkili bir şekilde devre dışı bırakır.
System::String fontsFolder = get_ArtifactsDir() + u"HtmlSaveOptions.FontSubsetting.Fonts";

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportFontResources(true);
options->set_FontsFolder(fontsFolder);
options->set_FontResourcesSubsettingSizeThreshold(fontResourcesSubsettingSizeThreshold);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.FontSubsetting.html", options);

System::ArrayPtr<System::String> fontFileNames = System::IO::Directory::GetFiles(fontsFolder)->LINQ_Where(static_cast<System::Func<System::String, bool>>(static_cast<std::function<bool(System::String s)>>([](System::String s) -> bool
{
    return s.EndsWith(u".ttf");
})))->LINQ_ToArray();

ASSERT_EQ(3, fontFileNames->get_Length());

for (System::String filename : fontFileNames)
{
    // Varsayılan olarak, üç yazı tipimizden her biri için .ttf dosyaları 700 MB'den fazla olacaktır.
    // Alt kümeleme, hepsini 30 MB'nin altına düşürecektir.
    auto fontFileInfo = System::MakeObject<System::IO::FileInfo>(filename);

    ASSERT_TRUE(fontFileInfo->get_Length() > 700000 || fontFileInfo->get_Length() < 30000);
    ASSERT_TRUE(System::Math::Max(fontResourcesSubsettingSizeThreshold, 30000) > System::MakeObject<System::IO::FileInfo>(filename)->get_Length());
}
```

## Ayrıca Bakınız

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
