---
title: "Aspose::Words::Markup::IStructuredDocumentTag::get_LockContents method"
linktitle: "get_LockContents"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Markup::IStructuredDocumentTag::get_LockContents method. عندما تُضبط على true، ستمنع هذه الخاصية المستخدم من تعديل محتويات هذا الـ SDT في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.markup/istructureddocumenttag/get_lockcontents/
---
## IStructuredDocumentTag::get_LockContents method


عند تعيينه إلى true، سيمنع هذا الخاصية المستخدم من تعديل محتويات هذا **SDT**.

```cpp
virtual bool Aspose::Words::Markup::IStructuredDocumentTag::get_LockContents()=0
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

* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
