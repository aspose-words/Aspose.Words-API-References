---
title: "Aspose::Words::Fonts::FontInfoCollection sınıfı"
linktitle: "FontInfoCollection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FontInfoCollection sınıfı. Bir belgede kullanılan yazı tiplerinin koleksiyonunu temsil eder. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.fonts/fontinfocollection/
---
## FontInfoCollection class


Bir belgede kullanılan yazı tiplerinin koleksiyonunu temsil eder. Daha fazla bilgi için, [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) dokümantasyon makalesini ziyaret edin.

```cpp
class FontInfoCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Fonts::FontInfo>>
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Contains](./contains/)(const System::String\&) | Koleksiyonun verilen isimde bir yazı tipi içerip içermediğini belirler. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Koleksiyonda bulunan eleman sayısını alır. |
| [get_EmbedSystemFonts](./get_embedsystemfonts/)() const | Belgeye Sistem yazı tiplerinin gömülüp gömülmeyeceğini belirtir. Bu özelliğin varsayılan değeri **false**'dur. Bu seçenek yalnızca [EmbedTrueTypeFonts](./get_embedtruetypefonts/) seçeneği **true** olarak ayarlandığında çalışır. |
| [get_EmbedTrueTypeFonts](./get_embedtruetypefonts/)() const | Belge kaydedildiğinde TrueType yazı tiplerinin gömülüp gömülmeyeceğini belirtir. Bu özelliğin varsayılan değeri **false**'dur. |
| [get_SaveSubsetFonts](./get_savesubsetfonts/)() const | Belgeyle gömülü TrueType yazı tiplerinin bir alt kümesinin kaydedilip kaydedilmeyeceğini belirtir. Bu özelliğin varsayılan değeri **false**'dur. Bu seçenek yalnızca [EmbedTrueTypeFonts](./get_embedtruetypefonts/) özelliği **true** olarak ayarlandığında çalışır. |
| [GetEnumerator](./getenumerator/)() override | Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilecek bir enumeratör nesnesi döndürür. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Belirtilen isimde bir yazı tipini alır. |
| [idx_get](./idx_get/)(int32_t) | Belirtilen indeksteki bir yazı tipini alır. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_EmbedSystemFonts](./set_embedsystemfonts/)(bool) | Ayarlayıcı [Aspose::Words::Fonts::FontInfoCollection::get_EmbedSystemFonts](./get_embedsystemfonts/). |
| [set_EmbedTrueTypeFonts](./set_embedtruetypefonts/)(bool) | Ayarlayıcı [Aspose::Words::Fonts::FontInfoCollection::get_EmbedTrueTypeFonts](./get_embedtruetypefonts/). |
| [set_SaveSubsetFonts](./set_savesubsetfonts/)(bool) | Ayarlayıcı [Aspose::Words::Fonts::FontInfoCollection::get_SaveSubsetFonts](./get_savesubsetfonts/). |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Açıklama |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Açıklamalar


Ögeler [FontInfo](../fontinfo/) nesneleridir.

Bu sınıfın örneklerini doğrudan oluşturmazsınız. Belgede tanımlı yazı tipleri koleksiyonuna erişmek için [FontInfos](../../aspose.words/documentbase/get_fontinfos/) özelliğini kullanın.

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

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
