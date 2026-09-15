---
title: "طريقة Aspose::Words::Markup::StructuredDocumentTag::get_LockContentControl"
linktitle: "get_LockContentControl"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Markup::StructuredDocumentTag::get_LockContentControl. عندما يتم تعيينها إلى true، سيمنع هذا الخاصية المستخدم من حذف هذا **SDT** في C++."
type: docs
weight: 22000
url: /ar/cpp/aspose.words.markup/structureddocumenttag/get_lockcontentcontrol/
---
## StructuredDocumentTag::get_LockContentControl method


عند تعيينه إلى **true**، ستمنع هذه الخاصية المستخدم من حذف هذه **SDT**.

```cpp
bool Aspose::Words::Markup::StructuredDocumentTag::get_LockContentControl() override
```


## أمثلة



يظهر كيفية تطبيق قيود التحرير على علامات المستند المنسقة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج علامة مستند منسق نصية عادية، والتي تعمل كصندوق نص يطلب من المستخدم ملئها.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// قم بتعيين الخاصية "LockContents" إلى "true" لمنع المستخدم من تعديل محتويات هذا الصندوق النصي.
tag->set_LockContents(true);
builder->Write(u"The contents of this structured document tag cannot be edited: ");
builder->InsertNode(tag);

tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// قم بتعيين الخاصية "LockContentControl" إلى "true" لمنع المستخدم من
// حذف هذه العلامة المستندية المنسقة يدويًا في Microsoft Word.
tag->set_LockContentControl(true);

builder->InsertParagraph();
builder->Write(u"This structured document tag cannot be deleted but its contents can be edited: ");
builder->InsertNode(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.Lock.docx");
```

## انظر أيضًا

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
