---
title: "Aspose::Words::WarningInfoCollection::idx_get yöntemi"
linktitle: "idx_get"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::WarningInfoCollection::idx_get yöntemi. C++'ta belirtilen indeksteki öğeyi alır."
type: docs
weight: 11000
url: /tr/cpp/aspose.words/warninginfocollection/idx_get/
---
## WarningInfoCollection::idx_get method


Belirtilen indeksteki öğeyi alır.

```cpp
System::SharedPtr<Aspose::Words::WarningInfo> Aspose::Words::WarningInfoCollection::idx_get(int32_t index)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| index | int32_t | Öğenin sıfır tabanlı indeksi. |

## Örnekler



Desteklenmeyen formatlarla ilgili uyarıların nasıl alınacağını gösterir.
```cpp
auto warnings = System::MakeObject<Aspose::Words::WarningInfoCollection>();
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_WarningCallback(warnings);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"FB2 document.fb2", loadOptions);

ASSERT_EQ(u"The original file load format is FB2, which is not supported by Aspose.Words. The file is loaded as an XML document.", warnings->idx_get(0)->get_Description());
ASSERT_EQ(1, warnings->get_Count());
```

## Ayrıca Bakınız

* Class [WarningInfo](../../warninginfo/)
* Class [WarningInfoCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
