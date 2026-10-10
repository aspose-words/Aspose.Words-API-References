---
title: "Aspose::Words::TabStopCollection::GetIndexByPosition yöntemi"
linktitle: "GetIndexByPosition"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::TabStopCollection::GetIndexByPosition yöntemi. C++'ta belirtilen konumdaki (nokta cinsinden) sekme durakının dizinini alır."
type: docs
weight: 9000
url: /tr/cpp/aspose.words/tabstopcollection/getindexbyposition/
---
## TabStopCollection::GetIndexByPosition method


Belirtilen konuma (puan cinsinden) sahip bir sekme durak noktasının dizinini alır.

```cpp
int32_t Aspose::Words::TabStopCollection::GetIndexByPosition(double position)
```


## Örnekler



Bir konumu kontrol ederek o konumda bir sekme durak olup olmadığını ve dizinini elde etmeyi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat()->get_TabStops();

// 30 mm konumunda bir sekme durak ekleyin.
tabStops->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(30), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

// \"GetIndexByPosition\" tarafından döndürülen \"0\" sonucu, bir sekme durakının
// 30 mm'de bu koleksiyonda mevcut olduğunu ve dizininin 0 olduğunu doğrular.
ASSERT_EQ(0, tabStops->GetIndexByPosition(Aspose::Words::ConvertUtil::MillimeterToPoint(30)));

// \"GetIndexByPosition\" tarafından döndürülen \"-1\" sonucu,
// bu koleksiyonda 60 mm konumunda bir sekme durak bulunmadığını gösterir.
ASSERT_EQ(-1, tabStops->GetIndexByPosition(Aspose::Words::ConvertUtil::MillimeterToPoint(60)));
```

## Ayrıca Bakınız

* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
