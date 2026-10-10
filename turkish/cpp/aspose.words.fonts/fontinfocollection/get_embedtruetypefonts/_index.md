---
title: "Aspose::Words::Fonts::FontInfoCollection::get_EmbedTrueTypeFonts metodu"
linktitle: "get_EmbedTrueTypeFonts"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FontInfoCollection::get_EmbedTrueTypeFonts metodu. Belge kaydedildiğinde TrueType yazı tiplerinin yerleştirilip yerleştirilmeyeceğini belirtir. Bu özelliğin C++'taki varsayılan değeri false'dur."
type: docs
weight: 9000
url: /tr/cpp/aspose.words.fonts/fontinfocollection/get_embedtruetypefonts/
---
## FontInfoCollection::get_EmbedTrueTypeFonts method


Belge kaydedildiğinde TrueType yazı tiplerinin gömülüp gömülmeyeceğini belirtir. Bu özelliğin varsayılan değeri **false**'dur.

```cpp
bool Aspose::Words::Fonts::FontInfoCollection::get_EmbedTrueTypeFonts() const
```

## Açıklamalar


TrueType yazı tiplerini yerleştirmek, başkalarının belgeyi oluşturulurken kullanılan aynı yazı tipleriyle görüntülemesini sağlar, ancak belge boyutunu önemli ölçüde artırabilir.

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
