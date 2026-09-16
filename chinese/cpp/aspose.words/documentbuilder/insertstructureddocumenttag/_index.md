---
title: "Aspose::Words::DocumentBuilder::InsertStructuredDocumentTag method"
linktitle: "InsertStructuredDocumentTag"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder::InsertStructuredDocumentTag 方法。将在 C++ 中向文档插入 StructuredDocumentTag。"
type: docs
weight: 46500
url: /zh/cpp/aspose.words/documentbuilder/insertstructureddocumenttag/
---
## DocumentBuilder::InsertStructuredDocumentTag method


将一个 [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) 插入文档。

```cpp
System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> Aspose::Words::DocumentBuilder::InsertStructuredDocumentTag(Aspose::Words::Markup::SdtType type)
```


### ReturnValue

刚插入的 [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) 节点。

## 示例



展示如何简单地插入 StructuredDocumentTag。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveTo(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(3));
// 注意，仅允许插入以下 StructuredDocumentTag 类型：
// SdtType.PlainText, SdtType.RichText, SdtType.Checkbox, SdtType.DropDownList,
// SdtType.ComboBox, SdtType.Picture, SdtType.Date.
// 插入的 StructuredDocumentTag 的标记级别将自动检测，并取决于插入位置。
// 添加的 StructuredDocumentTag 将继承光标位置的段落和字体格式。
System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> sdtPlain = builder->InsertStructuredDocumentTag(Aspose::Words::Markup::SdtType::PlainText);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.InsertStructuredDocumentTag.docx");
```

## 另见

* Class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* Enum [SdtType](../../../aspose.words.markup/sdttype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
