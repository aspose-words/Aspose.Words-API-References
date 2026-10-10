---
title: "Aspose::Words::HeaderFooterCollection class"
linktitle: "HeaderFooterCollection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::HeaderFooterCollection sınıfı. Bir Bölümün HeaderFooter düğümlerine tipli erişim sağlar. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 32000
url: /tr/cpp/aspose.words/headerfootercollection/
---
## HeaderFooterCollection class


Bir [Section](../section/) öğesinin [HeaderFooter](../headerfooter/) düğümlerine tipli erişim sağlar. Daha fazla bilgi edinmek için [Working with Headers and Footers](https://docs.aspose.com/words/cpp/working-with-headers-and-footers/) belge makalesini ziyaret edin.

```cpp
class HeaderFooterCollection : public Aspose::Words::NodeCollection
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Add](../nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Bir düğümü koleksiyonun sonuna ekler. |
| [Clear](../nodecollection/clear/)() | Bu koleksiyondaki ve belgedeki tüm düğümleri kaldırır. |
| [Contains](../nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Bir düğümün koleksiyonda olup olmadığını belirler. |
| [get_Count](../nodecollection/get_count/)() | Koleksiyondaki düğüm sayısını alır. |
| [GetEnumerator](../nodecollection/getenumerator/)() override | Düğümlerin koleksiyonu üzerinde basit bir "foreach" tarzı yineleme sağlar. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Verilen indeksde bir [HeaderFooter](../headerfooter/) alır. |
| [idx_get](./idx_get/)(Aspose::Words::HeaderFooterType) | Belirtilen türde bir [HeaderFooter](../headerfooter/) alır. |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Belirtilen düğümün sıfır tabanlı indeksini döndürür. |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Belirtilen indeksde bir düğümü koleksiyona ekler. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LinkToPrevious](./linktoprevious/)(bool) | Tüm başlıkları ve altbilgileri önceki bölümdeki karşılık gelen başlık ve altbilgilere bağlar veya bağlarını kaldırır. |
| [LinkToPrevious](./linktoprevious/)(Aspose::Words::HeaderFooterType, bool) | Belirtilen başlık veya altbilgiyi önceki bölümdeki karşılık gelen başlık veya altbilgiye bağlar veya bağını kaldırır. |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Düğümü koleksiyondan ve belgeden kaldırır. |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | Belirtilen indeksteki düğümü koleksiyondan ve belgeden kaldırır. |
| [ToArray](./toarray/)() | Tüm **HeaderFooter**'ları koleksiyondan yeni bir **HeaderFooter** dizisine kopyalar. |
| static [Type](./type/)() |  |
## Açıklamalar


Maksimum bir [HeaderFooter](../headerfooter/) olabilir.

her [HeaderFooterType](../headerfootertype/) için bir [Section](../section/) başına.

[HeaderFooter](../headerfooter/) objects can occur in any order in the collection.

## Örnekler



Bir üstbilgi ve altbilgi oluşturmayı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Bir üstbilgi oluşturun ve ona bir paragraf ekleyin. O paragraftaki metin
// bu bölümün her sayfasının üst kısmında, ana metnin üzerinde görünecek.
auto header = System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::HeaderPrimary);
doc->get_FirstSection()->get_HeadersFooters()->Add(header);

System::SharedPtr<Aspose::Words::Paragraph> para = header->AppendParagraph(u"My header.");

ASSERT_TRUE(header->get_IsHeader());
ASSERT_TRUE(para->get_IsEndOfHeaderFooter());

// Bir altbilgi oluşturun ve ona bir paragraf ekleyin. O paragraftaki metin
// bu bölümün her sayfasının alt kısmında, ana metnin altında görünecek.
auto footer = System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::FooterPrimary);
doc->get_FirstSection()->get_HeadersFooters()->Add(footer);

para = footer->AppendParagraph(u"My footer.");

ASSERT_FALSE(footer->get_IsHeader());
ASSERT_TRUE(para->get_IsEndOfHeaderFooter());

ASPOSE_ASSERT_EQ(footer, para->get_ParentStory());
ASPOSE_ASSERT_EQ(footer->get_ParentSection(), para->get_ParentSection());
ASPOSE_ASSERT_EQ(footer->get_ParentSection(), header->get_ParentSection());

doc->Save(get_ArtifactsDir() + u"HeaderFooter.Create.docx");
```


Bir belgeden tüm altbilgileri silmeyi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Header and footer types.docx");

// Her bölümü dolaşın ve her türlü altbilgiyi kaldırın.
for (auto&& section : System::IterateOver(doc->LINQ_OfType<System::SharedPtr<Aspose::Words::Section> >()))
{
    // Üstbilgi ve altbilgi türlerinin üç çeşidi vardır.
    // 1 -  \"First\" üstbilgi/altbilgi, yalnızca bir bölümün ilk sayfasında görünür.
    System::SharedPtr<Aspose::Words::HeaderFooter> footer = section->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterFirst);
    System::SharedPtr<Aspose::Words::HeaderFooter> condExpression = footer;
    if (condExpression != nullptr)
    {
        condExpression->Remove();
    }

    // 2 -  \"Primary\" üstbilgi/altbilgi, tek sayfalarda görünür.
    footer = section->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);
    System::SharedPtr<Aspose::Words::HeaderFooter> condExpression2 = footer;
    if (condExpression2 != nullptr)
    {
        condExpression2->Remove();
    }

    // 3 -  \"Even\" üstbilgi/altbilgi, çift sayfalarda görünür.
    footer = section->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterEven);
    System::SharedPtr<Aspose::Words::HeaderFooter> condExpression3 = footer;
    if (condExpression3 != nullptr)
    {
        condExpression3->Remove();
    }

    ASSERT_EQ(0, section->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
    {
        return !(System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsHeader();
    }))));
}

doc->Save(get_ArtifactsDir() + u"HeaderFooter.RemoveFooters.docx");
```

## Ayrıca Bakınız

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
