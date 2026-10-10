---
title: "Aspose::Words::Font::get_HighlightColor طريقة"
linktitle: "get_HighlightColor"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Font::get_HighlightColor طريقة. يسترجع أو يعيّن لون التظليل (المؤشر) في C++."
type: docs
weight: 17000
url: /ar/cpp/aspose.words/font/get_highlightcolor/
---
## Font::get_HighlightColor method


يحصل على أو يضبط لون التمييز (العلامة).

```cpp
System::Drawing::Color Aspose::Words::Font::get_HighlightColor()
```


## أمثلة



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
