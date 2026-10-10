---
title: "طريقة Aspose::Words::Markup::StructuredDocumentTag::get_Checked"
linktitle: "get_Checked"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Markup::StructuredDocumentTag::get_Checked. يحصل/يضبط الحالة الحالية لعنصر Checkbox SDT. القيمة الافتراضية لهذه الخاصية هي false في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words.markup/structureddocumenttag/get_checked/
---
## StructuredDocumentTag::get_Checked method


يحصل/يضبط الحالة الحالية لمربع الاختيار **SDT**. القيمة الافتراضية لهذه الخاصية هي **false**.

```cpp
bool Aspose::Words::Markup::StructuredDocumentTag::get_Checked()
```

## ملاحظات


الوصول إلى هذه الخاصية سيعمل فقط لأنواع SDT من [Checkbox](../../sdttype/).

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
