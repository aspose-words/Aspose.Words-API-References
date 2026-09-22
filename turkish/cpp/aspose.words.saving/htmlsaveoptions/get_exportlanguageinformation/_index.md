---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportLanguageInformation yöntemi"
linktitle: "get_ExportLanguageInformation"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportLanguageInformation yöntemi. Dil bilgisinin HTML, MHTML veya EPUB'a aktarılıp aktarılmayacağını belirtir. Varsayılan değer C++'da false'tur."
type: docs
weight: 20000
url: /tr/cpp/aspose.words.saving/htmlsaveoptions/get_exportlanguageinformation/
---
## HtmlSaveOptions::get_ExportLanguageInformation method


Dil bilgilerinin HTML, MHTML veya EPUB'a dışa aktarılıp aktarılmayacağını belirtir. Varsayılan değer **false**'tur.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportLanguageInformation() const
```

## Açıklamalar


Bu özellik **true** olarak ayarlandığında Aspose.Words, dili belirten belge öğelerinde **lang** HTML özniteliğini üretir. Bu, dil ile ilgili anlamsallığı korumak için gerekebilir.

## Örnekler



.html olarak kaydederken dil bilgisini nasıl koruyacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Metni farklı yerel ayarlarda biçimlendirirken yazmak için oluşturucuyu kullanın.
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-US")->get_LCID());
builder->Writeln(u"Hello world!");

builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-GB")->get_LCID());
builder->Writeln(u"Hello again!");

builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"ru-RU")->get_LCID());
builder->Write(u"Привет, мир!");

// Belgeyi HTML olarak kaydederken bir SaveOptions nesnesi geçebiliriz
// her biçimlendirilmiş metnin yerel ayarını korumak ya da atmak için.
// \"ExportLanguageInformation\" bayrağını \"true\" olarak ayarlarsak,
// çıktı HTML belgesi <span> etiketlerinin \"lang\" özniteliklerinde yerel ayarları içerecektir.
// \"ExportLanguageInformation\" bayrağını \"false\" olarak ayarlarsak,
// çıktı HTML belgesindeki metin herhangi bir yerel ayar bilgisi içermeyecektir.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportLanguageInformation(exportLanguageInformation);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportLanguageInformation.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportLanguageInformation.html");

if (exportLanguageInformation)
{
    ASSERT_TRUE(outDocContents.Contains(u"<span>Hello world!</span>"));
    ASSERT_TRUE(outDocContents.Contains(u"<span lang=\"en-GB\">Hello again!</span>"));
    ASSERT_TRUE(outDocContents.Contains(u"<span lang=\"ru-RU\">Привет, мир!</span>"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(u"<span>Hello world!</span>"));
    ASSERT_TRUE(outDocContents.Contains(u"<span>Hello again!</span>"));
    ASSERT_TRUE(outDocContents.Contains(u"<span>Привет, мир!</span>"));
}
```

## Ayrıca Bakınız

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
