---
title: "Aspose::Words::ParagraphFormat::get_LinesToDrop طريقة"
linktitle: "get_LinesToDrop"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::ParagraphFormat::get_LinesToDrop طريقة. يحصل على أو يضبط عدد أسطر نص الفقرة المستخدمة لحساب ارتفاع الحرف المتساقط في C++."
type: docs
weight: 22000
url: /ar/cpp/aspose.words/paragraphformat/get_linestodrop/
---
## ParagraphFormat::get_LinesToDrop method


يحصل أو يضبط عدد أسطر نص الفقرة المستخدمة لحساب ارتفاع الحرف الأول الكبير.

```cpp
int32_t Aspose::Words::ParagraphFormat::get_LinesToDrop()
```


## أمثلة



يظهر كيفية ضبط حجم الحرف المتساقط.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// عدّل خاصية "LinesToDrop" لتعيين الفقرة كحرف بارز في بداية الفقرة،
// سيحولها إلى حرف كبير مزخرف يزيّن الفقرة التالية.
// امنح هذه الخاصية القيمة 4 لتحديد ارتفاع الحرف البارز بما يعادل أربعة أسطر نصية.
builder->get_ParagraphFormat()->set_LinesToDrop(4);
builder->Writeln(u"H");

// أعد ضبط خاصية "LinesToDrop" إلى 0 لتحويل الفقرة التالية إلى فقرة عادية.
// سيتدفق النص في هذه الفقرة حول الحرف البارز.
builder->get_ParagraphFormat()->set_LinesToDrop(0);
builder->Writeln(u"ello world!");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.LinesToDrop.odt");
```

## انظر أيضًا

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
