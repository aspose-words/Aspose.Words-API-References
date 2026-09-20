---
title: "Aspose::Words::WarningInfoCollection::get_Count 方法"
linktitle: "get_Count"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::WarningInfoCollection::get_Count 方法。获取 C++ 中集合包含的元素数量。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words/warninginfocollection/get_count/
---
## WarningInfoCollection::get_Count method


获取集合中包含的元素数量。

```cpp
int32_t Aspose::Words::WarningInfoCollection::get_Count()
```


## 示例



展示如何获取关于不受支持格式的警告。
```cpp
auto warnings = System::MakeObject<Aspose::Words::WarningInfoCollection>();
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_WarningCallback(warnings);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"FB2 document.fb2", loadOptions);

ASSERT_EQ(u"The original file load format is FB2, which is not supported by Aspose.Words. The file is loaded as an XML document.", warnings->idx_get(0)->get_Description());
ASSERT_EQ(1, warnings->get_Count());
```

## 另见

* Class [WarningInfoCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
