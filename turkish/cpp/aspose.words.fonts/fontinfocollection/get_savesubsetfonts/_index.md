---
title: "Aspose::Words::Fonts::FontInfoCollection::get_SaveSubsetFonts yöntemi"
linktitle: "get_SaveSubsetFonts"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FontInfoCollection::get_SaveSubsetFonts yöntemi. Belgeyle birlikte gömülü TrueType yazı tiplerinin bir alt kümesinin kaydedilip kaydedilmeyeceğini belirtir. Bu özelliğin varsayılan değeri false'tur. Bu seçenek yalnızca C++'ta EmbedTrueTypeFonts özelliği true olarak ayarlandığında çalışır."
type: docs
weight: 10000
url: /tr/cpp/aspose.words.fonts/fontinfocollection/get_savesubsetfonts/
---
## FontInfoCollection::get_SaveSubsetFonts method


Belgeyle birlikte gömülü TrueType yazı tiplerinin bir alt kümesinin kaydedilip kaydedilmeyeceğini belirtir. Bu özelliğin varsayılan değeri **false**'tur. Bu seçenek yalnızca [EmbedTrueTypeFonts](../get_embedtruetypefonts/) özelliği **true** olarak ayarlandığında çalışır.

```cpp
bool Aspose::Words::Fonts::FontInfoCollection::get_SaveSubsetFonts() const
```


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
