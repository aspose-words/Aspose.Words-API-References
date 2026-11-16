---
title: Aspose::Words::WarningInfoCollection::get_Count method
linktitle: get_Count
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::WarningInfoCollection::get_Count method. Gets the number of elements contained in the collection in C++.'
type: docs
weight: 17500
url: /cpp/aspose.words/warninginfocollection/get_count/
---
## WarningInfoCollection::get_Count method


Gets the number of elements contained in the collection.

```cpp
int32_t Aspose::Words::WarningInfoCollection::get_Count()
```

## Examples


Shows how to get warnings about unsupported formats.

```cpp
auto warnings = System::MakeObject<Aspose::Words::WarningInfoCollection>();
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_WarningCallback(warnings);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"FB2 document.fb2", loadOptions);

ASSERT_EQ(warnings->idx_get(0)->get_Description(), (u"The original file load format is FB2, which is not supported by Aspose.Words. The file is loaded as an XML document."));
ASSERT_EQ(warnings->get_Count(), 1);
```
## See Also

* Class [WarningInfoCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
