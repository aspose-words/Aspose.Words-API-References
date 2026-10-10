---
title: "Aspose::Words::Font::get_Name طريقة"
linktitle: "get_Name"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Font::get_Name طريقة. يسترجع أو يعيّن اسم الخط في C++."
type: docs
weight: 25000
url: /ar/cpp/aspose.words/font/get_name/
---
## Font::get_Name method


يحصل على أو يضبط اسم الخط.

```cpp
System::String Aspose::Words::Font::get_Name()
```

## ملاحظات


عند الاسترجاع، يُعيد [NameAscii](../get_nameascii/).

عند التعيين، يعيّن [NameAscii](../get_nameascii/)، [NameBi](../get_namebi/)، [NameFarEast](../get_namefareast/) و [NameOther](../get_nameother/) إلى القيمة المحددة.

## أمثلة



يوضح كيفية إدراج نص منسق باستخدام [DocumentBuilder](../../documentbuilder/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// حدد تنسيق الخط، ثم أضف النص.
System::SharedPtr<Aspose::Words::Font> font = builder->get_Font();
font->set_Size(16);
font->set_Bold(true);
font->set_Color(System::Drawing::Color::get_Blue());
font->set_Name(u"Courier New");
font->set_Underline(Aspose::Words::Underline::Dash);

builder->Write(u"Hello world!");
```


يوضح كيفية تنسيق مقطع نصي باستخدام خاصية الخط الخاصة به.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");

System::SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);
doc->Save(get_ArtifactsDir() + u"Font.CreateFormattedRun.docx");
```

## انظر أيضًا

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
