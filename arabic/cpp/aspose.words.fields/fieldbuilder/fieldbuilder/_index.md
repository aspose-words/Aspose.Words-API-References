---
title: "منشئ Aspose::Words::Fields::FieldBuilder::FieldBuilder"
linktitle: "FieldBuilder"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "منشئ Aspose::Words::Fields::FieldBuilder::FieldBuilder. يهيئ نسخة من فئة FieldBuilder في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.fields/fieldbuilder/fieldbuilder/
---
## FieldBuilder::FieldBuilder constructor


يهيئ نسخة من فئة [FieldBuilder](../).

```cpp
Aspose::Words::Fields::FieldBuilder::FieldBuilder(Aspose::Words::Fields::FieldType fieldType)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| fieldType | Aspose::Words::Fields::FieldType | نوع الحقل الذي سيتم بناؤه. |

## أمثلة



يظهر كيفية إنشاء وإدراج حقل باستخدام منشئ الحقول.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// طريقة مريحة لإضافة محتوى نصي إلى مستند هي باستخدام منشئ المستند.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u" Hello world! This text is one Run, which is an inline node.");

// للحقل منشئ خاص به، يمكننا استخدامه لبناء شفرة الحقل قطعةً بقطعة.
// في هذه الحالة، سنقوم بإنشاء حقل BARCODE يمثل رمزًا بريديًا أمريكيًا،
// ثم نقوم بإدراجه أمام عنصر Run.
auto fieldBuilder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldBarcode);
fieldBuilder->AddArgument(u"90210");
fieldBuilder->AddSwitch(u"\\f", u"A");
fieldBuilder->AddSwitch(u"\\u");

fieldBuilder->BuildAndInsert(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0));

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.CreateWithFieldBuilder.docx");
```

## انظر أيضًا

* Enum [FieldType](../../fieldtype/)
* Class [FieldBuilder](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
