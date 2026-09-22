---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ResolveFontNames yöntemi"
linktitle: "get_ResolveFontNames"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ResolveFontNames yöntemi. Belge içinde kullanılan yazı tipi ailesi adlarının, C++'da HTML tabanlı formatlara yazılırken FontSettings'e göre çözülüp değiştirilip değiştirilmediğini belirtir."
type: docs
weight: 42000
url: /tr/cpp/aspose.words.saving/htmlsaveoptions/get_resolvefontnames/
---
## HtmlSaveOptions::get_ResolveFontNames method


Belge içinde kullanılan yazı tipi ailesi adlarının, HTML tabanlı formatlara yazılırken [FontSettings](../../../aspose.words/document/get_fontsettings/)'e göre çözülüp değiştirilip değiştirilmediğini belirtir.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ResolveFontNames() const
```

## Açıklamalar


Varsayılan olarak, bu seçenek **false** olarak ayarlanır ve yazı tipi ailesi adları kaynak belgelerde belirtildiği gibi HTML'ye yazılır. Yani, [FontSettings](../../../aspose.words/document/get_fontsettings/) yok sayılır ve yazı tipi ailesi adlarının hiçbir çözümü veya değiştirilmesi yapılmaz.

Bu seçenek **true** olarak ayarlanırsa, Aspose.Words [FontSettings](../../../aspose.words/document/get_fontsettings/) kullanarak kaynak belgede belirtilen her yazı tipi ailesi adını mevcut bir yazı tipi ailesinin adıyla eşleştirir ve gerektiği gibi yazı tipi ikamesi gerçekleştirir.

## Örnekler



HTML'ye yazılmadan önce tüm yazı tipi adlarının nasıl çözüleceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing font.docx");

// Bu belge, sahip olmadığımız bir yazı tipini adlandıran metin içerir.
ASSERT_FALSE(System::TestTools::IsNull(doc->get_FontInfos()->idx_get(u"28 Days Later")));

// Bu yazı tipini elde etmenin bir yolu yoksa ve tüm metni görüntüleyebilmek istiyorsak
// bu belgenin çıktısı olan HTML'de, başka bir yazı tipiyle ikame edebiliriz.
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Arial");
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_Enabled(true);

doc->set_FontSettings(fontSettings);

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
// Varsayılan olarak, bu seçenek 'False' olarak ayarlanır ve Aspose.Words, yazı tipi adlarını kaynak belgede belirtildiği gibi yazar.
saveOptions->set_ResolveFontNames(resolveFontNames);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ResolveFontNames.html", saveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ResolveFontNames.html");

ASSERT_TRUE(resolveFontNames ? System::Text::RegularExpressions::Regex::Match(outDocContents, u"<span style=\"font-family:Arial\">")->get_Success() : System::Text::RegularExpressions::Regex::Match(outDocContents, u"<span style=\"font-family:\'28 Days Later\'\">")->get_Success());
```

## Ayrıca Bakınız

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
