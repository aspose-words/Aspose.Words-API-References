---
title: "طريقة Aspose::Words::DocumentBuilder::PushFont"
linktitle: "PushFont"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::DocumentBuilder::PushFont. يحفظ تنسيق الأحرف الحالي على المكدس في C++."
type: docs
weight: 63000
url: /ar/cpp/aspose.words/documentbuilder/pushfont/
---
## DocumentBuilder::PushFont method


يحفظ تنسيق الأحرف الحالي على المكدس.

```cpp
void Aspose::Words::DocumentBuilder::PushFont()
```


## أمثلة



يوضح كيفية استخدام مكدس تنسيق منشئ المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// قم بإعداد تنسيق الخط، ثم اكتب النص الذي يسبق الارتباط.
builder->get_Font()->set_Name(u"Arial");
builder->get_Font()->set_Size(24);
builder->Write(u"To visit Google, hold Ctrl and click ");

// احفظ تكوين التنسيق الحالي على المكدس.
builder->PushFont();

// غيّر تنسيق المنشئ الحالي بتطبيق نمط جديد.
builder->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Hyperlink);
builder->InsertHyperlink(u"here", u"http://www.google.com", false);

ASSERT_EQ(System::Drawing::Color::get_Blue().ToArgb(), builder->get_Font()->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Underline::Single, builder->get_Font()->get_Underline());

// استعد تنسيق الخط الذي حفظناه مسبقًا وأزل العنصر من المكدس.
builder->PopFont();

ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), builder->get_Font()->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Underline::None, builder->get_Font()->get_Underline());

builder->Write(u". We hope you enjoyed the example.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.PushPopFont.docx");
```

## انظر أيضًا

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
