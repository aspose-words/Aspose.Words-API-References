---
title: "Aspose::Words::TabStop sınıfı"
linktitle: "TabStop"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::TabStop sınıfı. Tek bir özel sekme durağını temsil eder. TabStop nesnesi TabStopCollection koleksiyonunun bir üyesidir. Daha fazla bilgi için C++ belgeleri makalesini ziyaret edin."
type: docs
weight: 68000
url: /tr/cpp/aspose.words/tabstop/
---
## TabStop class


Tek bir özel sekme durağını temsil eder. [TabStop](./) nesnesi [TabStopCollection](../tabstopcollection/) koleksiyonunun bir üyesidir. Daha fazla bilgi için [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) belgeleri makalesini ziyaret edin.

```cpp
class TabStop : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::TabStop\>\&) | Belirtilen [TabStop](./) ile karşılaştırır. |
| [get_Alignment](./get_alignment/)() const | Bu sekme durağındaki metnin hizalamasını alır veya ayarlar. |
| [get_IsClear](./get_isclear/)() | Bu sekme durağı bu konumdaki mevcut sekme duraklarını temizlerse **true** döndürür. |
| [get_Leader](./get_leader/)() const | Sekme karakterinin altında gösterilen lider çizgi tipini alır veya ayarlar. |
| [get_Position](./get_position/)() | Sekme durağının konumunu puan cinsinden alır. |
| [GetHashCode](./gethashcode/)() const override | Bu nesne için karma kodunu hesaplar. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Alignment](./set_alignment/)(Aspose::Words::TabAlignment) | [Aspose::Words::TabStop::get_Alignment](./get_alignment/) için ayarlayıcı. |
| [set_Leader](./set_leader/)(Aspose::Words::TabLeader) | [Aspose::Words::TabStop::get_Leader](./get_leader/) için ayarlayıcı. |
| [TabStop](./tabstop/)(double) | Bu sınıfın yeni bir örneğini başlatır. |
| [TabStop](./tabstop/)(double, Aspose::Words::TabAlignment, Aspose::Words::TabLeader) | Bu sınıfın yeni bir örneğini başlatır. |
| static [Type](./type/)() |  |
## Açıklamalar


Normalde, bir sekme durağı bir sekme durağının bulunduğu konumu belirtir. Ancak sekme durakları üst stillerden devralınabildiği için, alt nesnenin belirli bir konumda sekme durağı olmadığını açıkça tanımlaması gerekebilir. Kalıtılmış bir sekme durağını belirli bir konumda temizlemek için bir [TabStop](./) nesnesi oluşturun ve [Alignment](./get_alignment/) özelliğini [Clear](../tabalignment/) olarak ayarlayın.

Daha fazla bilgi için [TabStopCollection](../tabstopcollection/) bölümüne bakın.

## Örnekler



İçindekiler tablosu (TOC) ile ilgili paragraflarda sağ sekme durağının konumunu nasıl değiştireceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table of contents.docx");

// TOC sonuç tabanlı stillere sahip tüm paragraflar arasında yineleme yapın; bu, TOC ile TOC9 arasındaki herhangi bir stildir.
for (auto&& para : System::IterateOver<Aspose::Words::Paragraph>(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)))
{
    if (para->get_ParagraphFormat()->get_Style()->get_StyleIdentifier() >= Aspose::Words::StyleIdentifier::Toc1 && para->get_ParagraphFormat()->get_Style()->get_StyleIdentifier() <= Aspose::Words::StyleIdentifier::Toc9)
    {
        // Bu paragrafta kullanılan ilk sekmeyi alın, bu sekme sayfa numaralarını hizalamak için kullanılmalıdır.
        System::SharedPtr<Aspose::Words::TabStop> tab = para->get_ParagraphFormat()->get_TabStops()->idx_get(0);

        // İlk varsayılan sekme durağını özel bir sekme durağı ile değiştirin.
        para->get_ParagraphFormat()->get_TabStops()->RemoveByPosition(tab->get_Position());
        para->get_ParagraphFormat()->get_TabStops()->Add(tab->get_Position() - 50, tab->get_Alignment(), tab->get_Leader());
    }
}

doc->Save(get_ArtifactsDir() + u"Styles.ChangeTocsTabStops.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
