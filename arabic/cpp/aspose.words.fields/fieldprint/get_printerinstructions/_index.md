---
title: "طريقة Aspose::Words::Fields::FieldPrint::get_PrinterInstructions"
linktitle: "get_PrinterInstructions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::FieldPrint::get_PrinterInstructions. يحصل أو يعيّن أحرف رموز التحكم الخاصة بالطابعة أو تعليمات PostScript في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.fields/fieldprint/get_printerinstructions/
---
## FieldPrint::get_PrinterInstructions method


يحصل أو يضبط أحرف رموز التحكم الخاصة بالطابعة أو تعليمات PostScript.

```cpp
System::String Aspose::Words::Fields::FieldPrint::get_PrinterInstructions()
```


## أمثلة



يعرض طريقة إدراج حقل PRINT.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"My paragraph");

// يمكن لحقل PRINT إرسال التعليمات إلى الطابعة.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldPrint>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldPrint, true));

// حدد المنطقة التي تنفذ الطابعة التعليمات عليها.
// في هذه الحالة، سيكون الفقرة التي تحتوي على حقل PRINT الخاص بنا.
field->set_PostScriptGroup(u"para");

// عند استخدامنا لطابعة تدعم PostScript لطباعة مستندنا،
// سيقوم هذا الأمر بتحويل المنطقة بالكامل التي حددناها في "field.PostScriptGroup" إلى اللون الأبيض.
field->set_PrinterInstructions(u"erasepage");

ASSERT_EQ(u" PRINT  erasepage \\p para", field->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.PRINT.docx");
```

## انظر أيضًا

* Class [FieldPrint](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
