---
title: "منشئ Aspose::Words::Markup::StructuredDocumentTag::StructuredDocumentTag"
linktitle: "StructuredDocumentTag"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "منشئ Aspose::Words::Markup::StructuredDocumentTag::StructuredDocumentTag. يهيئ مثيلاً جديداً لفئة Structured document tag في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.markup/structureddocumenttag/structureddocumenttag/
---
## StructuredDocumentTag::StructuredDocumentTag constructor


ينشئ مثيلاً جديداً لفئة **Structured document tag**.

```cpp
Aspose::Words::Markup::StructuredDocumentTag::StructuredDocumentTag(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, Aspose::Words::Markup::SdtType type, Aspose::Words::Markup::MarkupLevel level)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | المستند المالك. |
| نوع | Aspose::Words::Markup::SdtType | نوع عقدة SDT. |
| المستوى | Aspose::Words::Markup::MarkupLevel | مستوى عقدة SDT داخل المستند. |
## ملاحظات


الأنواع التالية من SDT يمكن إنشاؤها:

* [Checkbox](../../sdttype/)
* [DropDownList](../../sdttype/)
* [ComboBox](../../sdttype/)
* [Date](../../sdttype/)
* [BuildingBlockGallery](../../sdttype/)
* [Group](../../sdttype/)
* [Picture](../../sdttype/)
* [RichText](../../sdttype/)
* [PlainText](../../sdttype/)



## أمثلة



إظهار كيفية إنشاء علامة مستند منسقة على شكل مربع اختيار.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto sdtCheckBox = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Checkbox, Aspose::Words::Markup::MarkupLevel::Inline);
sdtCheckBox->set_Checked(true);

// يمكننا تعيين الرموز المستخدمة لتمثيل حالة الاختيار/عدم الاختيار لعنصر التحكم في محتوى مربع الاختيار.
sdtCheckBox->SetCheckedSymbol(0x00A9, u"Times New Roman");
sdtCheckBox->SetUncheckedSymbol(0x00AE, u"Times New Roman");

builder->InsertNode(sdtCheckBox);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.CheckBox.docx");
```

## انظر أيضًا

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Enum [SdtType](../../sdttype/)
* Enum [MarkupLevel](../../markuplevel/)
* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
