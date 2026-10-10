---
title: "Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts yöntemi"
linktitle: "get_AllowEmbeddingPostScriptFonts"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts yöntemi. Bir belge kaydedildiğinde TrueType yazı tipleri gömülürken PostScript konturlu yazı tiplerinin gömülmesine izin verilip verilmeyeceğini belirten bir boolean değer alır veya ayarlar. Varsayılan değer C++'da false'tur."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.saving/saveoptions/get_allowembeddingpostscriptfonts/
---
## SaveOptions::get_AllowEmbeddingPostScriptFonts method


Bir belge kaydedildiğinde TrueType yazı tiplerini gömerek PostScript konturlarıyla yazı tiplerinin gömülmesine izin verilip verilmediğini gösteren bir boolean değerini alır veya ayarlar. Varsayılan değer **false**.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts() const
```

## Açıklamalar


Not: Word, PostScript yazı tiplerini gömmez, ancak bu tür gömülü yazı tiplerine sahip belgeleri açabilir.

Bu seçenek yalnızca [FontInfos](../../../aspose.words/documentbase/get_fontinfos/) özelliğinin [EmbedTrueTypeFonts](../../../aspose.words.fonts/fontinfocollection/get_embedtruetypefonts/) **true** olarak ayarlandığında çalışır.

## Örnekler



PostScript yazı tipiyle belgeyi nasıl kaydedeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"PostScriptFont");
builder->Writeln(u"Some text with PostScript font.");

// Belgede kullanmak için PostScript ile yazı tipini yükleyin.
auto otf = System::MakeObject<Aspose::Words::Fonts::MemoryFontSource>(System::IO::File::ReadAllBytes(get_FontsDir() + u"AllegroOpen.otf"));
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({otf}));

// TrueType yazı tiplerini göm.
doc->get_FontInfos()->set_EmbedTrueTypeFonts(true);

// TrueType yazı tiplerini göderken PostScript yazı tiplerinin gömülmesine izin ver.
// Microsoft Word, PostScript yazı tiplerini gömmez, ancak bu tür gömülü yazı tiplerine sahip belgeleri açabilir.
System::SharedPtr<Aspose::Words::Saving::SaveOptions> saveOptions = Aspose::Words::Saving::SaveOptions::CreateSaveOptions(Aspose::Words::SaveFormat::Docx);
saveOptions->set_AllowEmbeddingPostScriptFonts(true);

doc->Save(get_ArtifactsDir() + u"Document.AllowEmbeddingPostScriptFonts.docx", saveOptions);
```

## Ayrıca Bakınız

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
