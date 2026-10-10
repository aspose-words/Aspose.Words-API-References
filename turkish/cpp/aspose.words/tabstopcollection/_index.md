---
title: "Aspose::Words::TabStopCollection sınıf"
linktitle: "TabStopCollection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::TabStopCollection sınıf. Bir paragraf veya stil için özel sekmeleri temsil eden TabStop nesnelerinin bir koleksiyonu. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 69000
url: /tr/cpp/aspose.words/tabstopcollection/
---
## TabStopCollection class


Bir paragraf veya stil için özel sekmeleri temsil eden [TabStop](../tabstop/) nesnelerinin bir koleksiyonu. Daha fazla bilgi edinmek için [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) belge makalesini ziyaret edin.

```cpp
class TabStopCollection : public Aspose::Words::InternableComplexAttr,
                          public Aspose::Words::IExpandableAttr
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::TabStop\>\&) | Koleksiyonda bir sekme durak noktasını ekler veya değiştirir. |
| [Add](./add/)(double, Aspose::Words::TabAlignment, Aspose::Words::TabLeader) | Koleksiyonda bir sekme durak noktasını ekler veya değiştirir. |
| [After](./after/)(double) | Belirtilen konumun sağındaki ilk sekme durak noktasını alır. |
| [Before](./before/)(double) | Belirtilen konumun solundaki ilk sekme durak noktasını alır. |
| [Clear](./clear/)() | Tüm sekme durak noktalarını siler. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::TabStopCollection\>\&) | Belirtilen [TabStopCollection](./) değer olarak mevcut [TabStopCollection](./) ile eşit olup olmadığını belirler. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Belirtilen nesnenin mevcut nesneyle değer olarak eşit olup olmadığını belirler. |
| [get_Count](./get_count/)() | Koleksiyondaki sekme durak noktalarının sayısını alır. |
| [GetHashCode](./gethashcode/)() const override | Bu tip için bir karma (hash) işlevi olarak hizmet verir. |
| [GetIndexByPosition](./getindexbyposition/)(double) | Belirtilen konuma (puan cinsinden) sahip bir sekme durak noktasının dizinini alır. |
| [GetPositionByIndex](./getpositionbyindex/)(int32_t) | Belirtilen dizindeki sekme durak noktasının konumunu (puan cinsinden) alır. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Verilen dizindeki bir sekme durak noktasını alır. |
| [idx_get](./idx_get/)(double) | Belirtilen konumdaki bir sekme durak noktasını alır. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [RemoveByIndex](./removebyindex/)(int32_t) | Koleksiyondan belirtilen dizindeki bir sekme durak noktasını kaldırır. |
| [RemoveByPosition](./removebyposition/)(double) | Koleksiyondan belirtilen konumdaki bir sekme durak noktasını kaldırır. |
| static [Type](./type/)() |  |
## Açıklamalar


Microsoft Word belgelerinde, bir sekme durak noktası bir paragraf stilinin özelliklerinde veya doğrudan bir paragrafın özelliklerinde tanımlanabilir. Bir stil başka bir stile dayanabilir. Bu nedenle, belirli bir nesne için tam sekme durak noktası kümesi, bu nesne üzerinde doğrudan tanımlanan sekme durak noktaları ile üst stil(ler)den miras alınan sekme durak noktalarının bir kombinasyonudur.

Aspose.Words'ta, bir paragraf veya stil için bir [TabStopCollection](./) elde ettiğinizde, yalnızca bu paragraf veya stil için doğrudan tanımlanan özel sekme durak noktalarını içerir. Koleksiyon, üst stillerde tanımlanan sekme durak noktalarını veya varsayılan sekme durak noktalarını içermez.

## Örnekler



Bir belgenin sekme durak noktası koleksiyonuyla nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = builder->get_ParagraphFormat()->get_TabStops();

// 72 puan, Microsoft Word sekme durak cetvelinde bir "inç"tir.
tabStops->Add(System::MakeObject<Aspose::Words::TabStop>(72.0));
tabStops->Add(System::MakeObject<Aspose::Words::TabStop>(432.0, Aspose::Words::TabAlignment::Right, Aspose::Words::TabLeader::Dashes));

ASSERT_EQ(2, tabStops->get_Count());
ASSERT_FALSE(tabStops->idx_get(0)->get_IsClear());
ASSERT_FALSE(System::ObjectExt::Equals(tabStops->idx_get(0), tabStops->idx_get(1)));

// Her "tab" karakteri, oluşturucunun imlecini bir sonraki sekme durak noktasının konumuna götürür.
builder->Writeln(u"Start\tTab 1\tTab 2");

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(2, paragraphs->get_Count());

// Her paragraf, değerlerini belge oluşturucusunun sekme durak noktası koleksiyonundan kopyalayan kendi sekme durak noktası koleksiyonunu alır.
ASPOSE_ASSERT_EQ(paragraphs->idx_get(0)->get_ParagraphFormat()->get_TabStops(), paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops());
ASPOSE_ASSERT_NS(paragraphs->idx_get(0)->get_ParagraphFormat()->get_TabStops(), paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops());

// Bir sekme durak noktası koleksiyonu, belirli konumlardan önce ve sonra bulunan TabStop'lara işaret edebilir.
ASPOSE_ASSERT_EQ(72.0, tabStops->Before(100.0)->get_Position());
ASPOSE_ASSERT_EQ(432.0, tabStops->After(100.0)->get_Position());

// Varsayılan sekme davranışına geri dönmek için bir paragrafın sekme durak noktası koleksiyonunu temizleyebiliriz.
paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops()->Clear();

ASSERT_EQ(0, paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops()->get_Count());

doc->Save(get_ArtifactsDir() + u"TabStopCollection.TabStopCollection.docx");
```

## Ayrıca Bakınız

* Class [InternableComplexAttr](../internablecomplexattr/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
