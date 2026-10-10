---
title: "Aspose::Words::Font::get_Superscript طريقة"
linktitle: "get_Superscript"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Font::get_Superscript طريقة. صحيح إذا كان الخط مُنسقًا كقيد علوي في C++."
type: docs
weight: 46000
url: /ar/cpp/aspose.words/font/get_superscript/
---
## Font::get_Superscript method


صحيح إذا كان الخط منسقًا كحرف علوي.

```cpp
bool Aspose::Words::Font::get_Superscript()
```


## أمثلة



يوضح كيفية تنسيق النص لإزاحة موضعه.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto para = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

// ارفع هذا المقطع النصي 5 نقاط فوق الخط الأساسي.
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Raised text. ");
run->get_Font()->set_Position(5);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// اخفض هذا المقطع النصي 10 نقاط تحت الخط الأساسي.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Lowered text. ");
run->get_Font()->set_Position(-10);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// أضف مقطع نص عادي.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Text in its default position. ");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// أضف مقطع نص يظهر كحرف سفلي.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Subscript. ");
run->get_Font()->set_Subscript(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// أضف مقطع نص يظهر كحرف علوي.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Superscript.");
run->get_Font()->set_Superscript(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Font.PositionSubscript.docx");
```

## انظر أيضًا

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
