---
title: "Aspose::Words::ImportFormatOptions::get_MergePastedLists 方法"
linktitle: "get_MergePastedLists"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ImportFormatOptions::get_MergePastedLists 方法。获取或设置一个布尔值，指定粘贴的列表是否会与周围的列表合并。默认值在 C++ 中为 false。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words/importformatoptions/get_mergepastedlists/
---
## ImportFormatOptions::get_MergePastedLists method


获取或设置一个布尔值，指定粘贴的列表是否会与周围的列表合并。默认值为 **false**。

```cpp
bool Aspose::Words::ImportFormatOptions::get_MergePastedLists() const
```


## 示例



展示如何合并文档中的列表。
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List item.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List destination.docx");

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_MergePastedLists(true);

// 将 "MergePastedLists" 属性设置为 "true"，粘贴的列表将与周围的列表合并。
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::UseDestinationStyles, options);

dstDoc->Save(get_ArtifactsDir() + u"Document.MergePastedLists.docx");
```

## 另见

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
