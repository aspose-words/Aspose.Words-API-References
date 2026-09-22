---
title: "Aspose::Words::DocumentBase::get_Styles yöntemi"
linktitle: "get_Styles"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBase::get_Styles yöntemi. C++'ta bu belgede kullanılan yazı tiplerinin özelliklerine erişim sağlar."
type: docs
weight: 4000
url: /tr/cpp/aspose.words/documentbase/get_fontinfos/
---
## DocumentBase::get_FontInfos method


Bu belgede kullanılan yazı tiplerinin özelliklerine erişim sağlar.

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> Aspose::Words::DocumentBase::get_FontInfos() const
```

## Açıklamalar


Bu yazı tipi tanımları koleksiyonu, belgeden olduğu gibi yüklenir. [Font](../../font/) tanımları bazı belgelerde isteğe bağlı, eksik veya tam olmayabilir.

Belirli bir yazı tipinin belgede kullanıldığını doğrulamak için bu koleksiyona güvenmeyin. Bu koleksiyonu yalnızca belgede kullanılabilecek yazı tipleri hakkında bilgi almak için kullanmalısınız.

## Örnekler



Bir belgede mevcut olan yazı tiplerinin ayrıntılarını nasıl yazdıracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> allFonts = doc->get_FontInfos();

// Belgedeki kullanılan ve kullanılmayan tüm yazı tiplerini yazdırın.
for (int32_t i = 0; i < allFonts->get_Count(); i++)
{
    std::cout << System::String::Format(u"Font index #{0}", i) << std::endl;
    std::cout << System::String::Format(u"\tName: {0}", allFonts->idx_get(i)->get_Name()) << std::endl;
    std::cout << System::String::Format(u"\tIs {0}a trueType font", (allFonts->idx_get(i)->get_IsTrueType() ? System::String(u"") : System::String(u"not "))) << std::endl;
}
```


Gömülü TrueType yazı tipleriyle bir belgenin nasıl kaydedileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> fontInfos = doc->get_FontInfos();
fontInfos->set_EmbedTrueTypeFonts(embedAllFonts);
fontInfos->set_EmbedSystemFonts(embedAllFonts);
fontInfos->set_SaveSubsetFonts(embedAllFonts);

doc->Save(get_ArtifactsDir() + u"Font.FontInfoCollection.docx");
```

## Ayrıca Bakınız

* Class [FontInfoCollection](../../../aspose.words.fonts/fontinfocollection/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
