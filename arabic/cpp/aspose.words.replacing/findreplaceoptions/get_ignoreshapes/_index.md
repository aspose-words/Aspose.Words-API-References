---
title: "طريقة Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreShapes"
linktitle: "get_IgnoreShapes"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreShapes. يحصل على أو يضبط قيمة منطقية تشير إلى ما إذا كان يجب تجاهل الأشكال داخل النص. القيمة الافتراضية هي false في C++."
type: docs
weight: 11500
url: /ar/cpp/aspose.words.replacing/findreplaceoptions/get_ignoreshapes/
---
## FindReplaceOptions::get_IgnoreShapes method


يحصل أو يعيّن قيمة منطقية تشير إلى ما إذا كان يجب تجاهل الأشكال داخل النص. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreShapes() const
```


## أمثلة



يوضح كيفية تجاهل الأشكال أثناء استبدال النص.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Balloon, 200, 200);
builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

auto findReplaceOptions = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
findReplaceOptions->set_IgnoreShapes(true);
builder->get_Document()->get_Range()->Replace(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.Lorem ipsum dolor sit amet, consectetur adipiscing elit.", u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.", findReplaceOptions);
ASSERT_EQ(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.", builder->get_Document()->GetText().Trim());
```

## انظر أيضًا

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
