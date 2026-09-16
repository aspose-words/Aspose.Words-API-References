---
title: "Aspose::Words::Markup::IStructuredDocumentTag::get_LockContentControl 方法"
linktitle: "get_LockContentControl"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::IStructuredDocumentTag::get_LockContentControl 方法。设置为 true 时，此属性将禁止用户在 C++ 中删除此结构化文档标签（SDT）。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.markup/istructureddocumenttag/get_lockcontentcontrol/
---
## IStructuredDocumentTag::get_LockContentControl method


设置为 true 时，此属性将阻止用户删除此 **SDT**。

```cpp
virtual bool Aspose::Words::Markup::IStructuredDocumentTag::get_LockContentControl()=0
```


## 示例



展示如何对结构化文档标签应用编辑限制。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入一个纯文本结构化文档标签，它充当提示用户填写的文本框。
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// 将 "LockContents" 属性设置为 "true"，以禁止用户编辑此文本框的内容。
tag->set_LockContents(true);
builder->Write(u"The contents of this structured document tag cannot be edited: ");
builder->InsertNode(tag);

tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// 将 "LockContentControl" 属性设置为 "true"，以禁止用户
// 在 Microsoft Word 中手动删除此结构化文档标签。
tag->set_LockContentControl(true);

builder->InsertParagraph();
builder->Write(u"This structured document tag cannot be deleted but its contents can be edited: ");
builder->InsertNode(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.Lock.docx");
```

## 另见

* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
