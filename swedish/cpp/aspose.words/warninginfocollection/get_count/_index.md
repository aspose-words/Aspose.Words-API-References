---
title: "Aspose::Words::WarningInfoCollection::get_Count‑metod"
linktitle: "get_Count"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::WarningInfoCollection::get_Count‑metod. Hämtar antalet element som finns i samlingen i C++."
type: docs
weight: 8000
url: /sv/cpp/aspose.words/warninginfocollection/get_count/
---
## WarningInfoCollection::get_Count method


Hämtar antalet element som finns i samlingen.

```cpp
int32_t Aspose::Words::WarningInfoCollection::get_Count()
```


## Exempel



Visar hur man får varningar om format som inte stöds.
```cpp
auto warnings = System::MakeObject<Aspose::Words::WarningInfoCollection>();
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_WarningCallback(warnings);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"FB2 document.fb2", loadOptions);

ASSERT_EQ(u"The original file load format is FB2, which is not supported by Aspose.Words. The file is loaded as an XML document.", warnings->idx_get(0)->get_Description());
ASSERT_EQ(1, warnings->get_Count());
```

## Se även

* Class [WarningInfoCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
