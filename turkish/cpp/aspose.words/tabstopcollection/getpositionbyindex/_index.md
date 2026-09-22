---
title: "Aspose::Words::TabStopCollection::GetPositionByIndex method"
linktitle: "GetPositionByIndex"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::TabStopCollection::GetPositionByIndex yöntemi. Belirtilen dizindeki sekme durakının konumunu (nokta cinsinden) C++'ta alır."
type: docs
weight: 10000
url: /tr/cpp/aspose.words/tabstopcollection/getpositionbyindex/
---
## TabStopCollection::GetPositionByIndex method


Belirtilen dizindeki sekme durak noktasının konumunu (puan cinsinden) alır.

```cpp
double Aspose::Words::TabStopCollection::GetPositionByIndex(int32_t index)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| index | int32_t | Sekme durakları koleksiyonundaki bir dizin. |

### ReturnValue

Sekme durakının konumu.

## Örnekler



Sekme durakını diziniyle bulmayı ve konumunu doğrulamayı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat()->get_TabStops();

tabStops->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(30), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
tabStops->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(60), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

// Koleksiyondaki ikinci sekme durakının konumunu doğrulayın.
ASSERT_NEAR(Aspose::Words::ConvertUtil::MillimeterToPoint(60), tabStops->GetPositionByIndex(1), 0.1);
```

## Ayrıca Bakınız

* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
