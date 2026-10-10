---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageSetup metodu"
linktitle: "get_ExportPageSetup"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageSetup metodu. Sayfa ayarının HTML, MHTML veya EPUB'a aktarılıp aktarılmayacağını belirtir. Varsayılan değer C++'de false'tur."
type: docs
weight: 24000
url: /tr/cpp/aspose.words.saving/htmlsaveoptions/get_exportpagesetup/
---
## HtmlSaveOptions::get_ExportPageSetup method


Sayfa ayarının HTML, MHTML veya EPUB formatına aktarılıp aktarılmayacağını belirtir. Varsayılan değer **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageSetup() const
```

## Açıklamalar


Aspose.Words belge modelindeki her [Section](../../../aspose.words/section/) [PageSetup](../../../aspose.words/pagesetup/) sınıfı aracılığıyla sayfa ayarı bilgisi sağlar. Bir belgeyi HTML formatına dışa aktarırken bu bilgiyi sonraki kullanım için tutmanız gerekebilir. Özellikle, sayfa ayarı sayfalı ortamda (yazdırma) görüntüleme veya yerel Microsoft Word dosya formatlarına (DOCX, DOC, RTF, WML) sonraki dönüşüm için önemli olabilir.

Çoğu durumda HTML, sayfalama yapılmadığı tarayıcılarda görüntülenmek üzere tasarlanmıştır. Bu nedenle bu özellik varsayılan olarak devre dışıdır.

## Örnekler



HTML olarak kaydederken bölüm yapısını/sayfa ayarı bilgisini koruyup korumayacağınızı nasıl karar vereceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_TopMargin(36.0);
pageSetup->set_BottomMargin(36.0);
pageSetup->set_PaperSize(Aspose::Words::PaperSize::A5);

// Belgeyi HTML olarak kaydederken bir SaveOptions nesnesi geçebiliriz
// sayfa ayarı ayarlarını koruyup korumayacağınıza karar vermek için.
// Eğer "ExportPageSetup" bayrağını "true" olarak ayarlarsak, çıktı HTML belgesi sayfa ayarı yapılandırmamızı içerecektir.
// Eğer "ExportPageSetup" bayrağını "false" olarak ayarlarsak, kaydetme işlemi sayfa ayarı ayarlarımızı atar
// ilk bölüm için ve her iki bölüm de aynı görünecek.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportPageSetup(exportPageSetup);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportPageSetup.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportPageSetup.html");

if (exportPageSetup)
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<style type=\"text/css\">") + u"@page Section_1 { size:419.55pt 595.3pt; margin:36pt 70.85pt; -aw-footer-distance:35.4pt; -aw-header-distance:35.4pt }" + u"@page Section_2 { size:612pt 792pt; margin:70.85pt; -aw-footer-distance:35.4pt; -aw-header-distance:35.4pt }" + u"div.Section_1 { page:Section_1 }div.Section_2 { page:Section_2 }" + u"</style>"));

    ASSERT_TRUE(outDocContents.Contains(System::String(u"<div class=\"Section_1\">") + u"<p style=\"margin-top:0pt; margin-bottom:0pt\">" + u"<span>Section 1</span>" + u"</p>" + u"</div>"));
}
else
{
    ASSERT_FALSE(outDocContents.Contains(u"style type=\"text/css\">"));

    ASSERT_TRUE(outDocContents.Contains(System::String(u"<div>") + u"<p style=\"margin-top:0pt; margin-bottom:0pt\">" + u"<span>Section 1</span>" + u"</p>" + u"</div>"));
}
```

## Ayrıca Bakınız

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
