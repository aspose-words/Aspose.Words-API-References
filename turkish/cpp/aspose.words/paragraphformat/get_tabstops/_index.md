---
title: "Aspose::Words::ParagraphFormat::get_TabStops yöntemi"
linktitle: "get_TabStops"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ParagraphFormat::get_TabStops yöntemi. C++'ta bu nesne için tanımlanan özel sekme duraklarının koleksiyonunu alır."
type: docs
weight: 40000
url: /tr/cpp/aspose.words/paragraphformat/get_tabstops/
---
## ParagraphFormat::get_TabStops method


Bu nesne için tanımlanan özel sekme durakları koleksiyonunu alır.

```cpp
System::SharedPtr<Aspose::Words::TabStopCollection> Aspose::Words::ParagraphFormat::get_TabStops()
```


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

* Class [TabStopCollection](../../tabstopcollection/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
