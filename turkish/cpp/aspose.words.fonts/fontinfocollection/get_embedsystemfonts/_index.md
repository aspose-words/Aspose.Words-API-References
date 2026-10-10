---
title: "Aspose::Words::Fonts::FontInfoCollection::get_EmbedSystemFonts metodu"
linktitle: "get_EmbedSystemFonts"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FontInfoCollection::get_EmbedSystemFonts metodu. Belgeye Sistem yazı tiplerinin yerleştirilip yerleştirilmeyeceğini belirtir. Bu özelliğin varsayılan değeri false'dur. Bu seçenek yalnızca C++'ta EmbedTrueTypeFonts seçeneği true olarak ayarlandığında çalışır."
type: docs
weight: 8000
url: /tr/cpp/aspose.words.fonts/fontinfocollection/get_embedsystemfonts/
---
## FontInfoCollection::get_EmbedSystemFonts method


Belgeye Sistem yazı tiplerinin yerleştirilip yerleştirilmeyeceğini belirtir. Bu özelliğin varsayılan değeri **false**'dur. Bu seçenek yalnızca [EmbedTrueTypeFonts](../get_embedtruetypefonts/) seçeneği **true** olarak ayarlandığında çalışır.

```cpp
bool Aspose::Words::Fonts::FontInfoCollection::get_EmbedSystemFonts() const
```

## Açıklamalar


Bu özelliği **true** olarak ayarlamak, kullanıcının Doğu Asya sisteminde olması ve sisteminde o dil için yazı tipleri bulunmayan diğer kişiler tarafından okunabilir bir belge oluşturmak istemesi durumunda faydalıdır. Örneğin, Japon sisteminde bir kullanıcı, Japonca belgenin tüm sistemlerde okunabilir olması için yazı tiplerini belgeye yerleştirmeyi seçebilir.

Bu seçenek yalnızca DOC, DOCX ve RTF formatları için çalışır.

## Örnekler



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

* Class [FontInfoCollection](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
