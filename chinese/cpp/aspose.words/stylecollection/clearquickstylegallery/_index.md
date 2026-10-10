---
title: "Aspose::Words::StyleCollection::ClearQuickStyleGallery 方法"
linktitle: "ClearQuickStyleGallery"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::StyleCollection::ClearQuickStyleGallery 方法。移除 C++ 中快速样式库面板中的所有样式。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words/stylecollection/clearquickstylegallery/
---
## StyleCollection::ClearQuickStyleGallery method


从快速 [Style](../../style/) 库面板中移除所有样式。

```cpp
void Aspose::Words::StyleCollection::ClearQuickStyleGallery()
```


## 示例



展示如何从 [Style](../../style/) 库面板中移除样式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
// 注意，删除样式目前仅在 DOCX 格式下有效。
doc->get_Styles()->ClearQuickStyleGallery();

doc->Save(get_ArtifactsDir() + u"Styles.RemoveStylesFromStyleGallery.docx");
```

## 另见

* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
