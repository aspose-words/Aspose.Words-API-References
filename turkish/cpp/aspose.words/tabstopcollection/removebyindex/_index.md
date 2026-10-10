---
title: "Aspose::Words::TabStopCollection::RemoveByIndex yöntemi"
linktitle: "RemoveByIndex"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::TabStopCollection::RemoveByIndex yöntemi. C++'ta belirtilen indeksteki sekme durağını koleksiyondan kaldırır."
type: docs
weight: 14000
url: /tr/cpp/aspose.words/tabstopcollection/removebyindex/
---
## TabStopCollection::RemoveByIndex method


Koleksiyondan belirtilen dizindeki bir sekme durak noktasını kaldırır.

```cpp
void Aspose::Words::TabStopCollection::RemoveByIndex(int32_t index)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| index | int32_t | Sekme durakları koleksiyonundaki bir dizin. |

## Örnekler



Bir belgedeki sekme durağını indeksine göre seçip kaldırmanın nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat()->get_TabStops();

tabStops->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(30), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
tabStops->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(60), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

ASSERT_EQ(2, tabStops->get_Count());

// İlk sekme durağını kaldır.
tabStops->RemoveByIndex(0);

ASSERT_EQ(1, tabStops->get_Count());

doc->Save(get_ArtifactsDir() + u"TabStopCollection.RemoveByIndex.docx");
```

## Ayrıca Bakınız

* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
