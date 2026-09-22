---
title: "طريقة Aspose::Words::DocumentBuilder::InsertStructuredDocumentTag"
linktitle: "InsertStructuredDocumentTag"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::DocumentBuilder::InsertStructuredDocumentTag. تُدرج StructuredDocumentTag في المستند باستخدام C++."
type: docs
weight: 46500
url: /ar/cpp/aspose.words/documentbuilder/insertstructureddocumenttag/
---
## DocumentBuilder::InsertStructuredDocumentTag method


تُدرج [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) في المستند.

```cpp
System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> Aspose::Words::DocumentBuilder::InsertStructuredDocumentTag(Aspose::Words::Markup::SdtType type)
```


### ReturnValue

العنصر [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) الذي تم إدراجه للتو.

## أمثلة



يوضح كيفية إدراج علامة مستند مُنظمة ببساطة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveTo(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(3));
// ملاحظة، أنه يُسمح فقط بأنواع StructuredDocumentTag التالية للإدراج:
// SdtType.PlainText, SdtType.RichText, SdtType.Checkbox, SdtType.DropDownList,
// SdtType.ComboBox, SdtType.Picture, SdtType.Date.
// سيتم اكتشاف مستوى العلامة المُنشأة StructuredDocumentTag تلقائيًا ويعتمد على الموضع الذي يتم الإدراج فيه.
// ستورث StructuredDocumentTag المضافة تنسيق الفقرة والخط من موضع المؤشر.
System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> sdtPlain = builder->InsertStructuredDocumentTag(Aspose::Words::Markup::SdtType::PlainText);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.InsertStructuredDocumentTag.docx");
```

## انظر أيضًا

* Class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* Enum [SdtType](../../../aspose.words.markup/sdttype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
