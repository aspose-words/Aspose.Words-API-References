---
title: "طريقة Aspose::Words::Markup::StructuredDocumentTag::SetUncheckedSymbol"
linktitle: "SetUncheckedSymbol"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Markup::StructuredDocumentTag::SetUncheckedSymbol. يحدد الرمز المستخدم لتمثيل الحالة غير المحددة لعنصر تحكم محتوى مربع الاختيار في C++."
type: docs
weight: 59000
url: /ar/cpp/aspose.words.markup/structureddocumenttag/setuncheckedsymbol/
---
## StructuredDocumentTag::SetUncheckedSymbol method


يضبط الرمز المستخدم لتمثيل الحالة غير المحددة لمربع اختيار عنصر التحكم بالمحتوى.

```cpp
void Aspose::Words::Markup::StructuredDocumentTag::SetUncheckedSymbol(int32_t characterCode, const System::String &fontName)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| characterCode | int32_t | رمز الحرف للرمز المحدد. |
| fontName | const System::String\& | اسم الخط الذي يحتوي على الرمز. |
## ملاحظات


ستعمل هذه الطريقة فقط لأنواع SDT من نوع [Checkbox](../../sdttype/).

ستحدث استثناء لجميع أنواع SDT الأخرى.

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

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
