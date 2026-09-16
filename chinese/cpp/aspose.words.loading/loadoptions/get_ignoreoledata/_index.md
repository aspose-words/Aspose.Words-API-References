---
title: "Aspose::Words::Loading::LoadOptions::get_IgnoreOleData 方法"
linktitle: "get_IgnoreOleData"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::LoadOptions::get_IgnoreOleData 方法。指定是否在 C++ 中忽略 OLE 数据。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words.loading/loadoptions/get_ignoreoledata/
---
## LoadOptions::get_IgnoreOleData method


指定是否忽略 OLE 数据。

```cpp
bool Aspose::Words::Loading::LoadOptions::get_IgnoreOleData() const
```

## 备注


忽略 OLE 数据可能在目标格式不支持 OLE 对象的情况下，减少内存消耗并提升性能且不会丢失数据。

默认值为 **false**。

## 示例



展示如何在加载时忽略 OLE 数据。
```cpp
// 忽略 OLE 数据可能减少内存消耗并提升性能
// 在目标格式不支持 OLE 对象的情况下，不会丢失数据。
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_IgnoreOleData(true);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE objects.docx", loadOptions);

doc->Save(get_ArtifactsDir() + u"LoadOptions.IgnoreOleData.docx");
```

## 另见

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
