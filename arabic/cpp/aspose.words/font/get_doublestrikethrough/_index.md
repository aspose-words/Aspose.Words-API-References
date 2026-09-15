---
title: "طريقة Aspose::Words::Font::get_DoubleStrikeThrough"
linktitle: "get_DoubleStrikeThrough"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Font::get_DoubleStrikeThrough method. صحيح إذا كان الخط مُنسقًا كنص بخط مزدوج مشطوب في C++."
type: docs
weight: 11000
url: /ar/cpp/aspose.words/font/get_doublestrikethrough/
---
## Font::get_DoubleStrikeThrough method


صحيح إذا كان الخط مُنسقًا كنص مع شطب مزدوج.

```cpp
bool Aspose::Words::Font::get_DoubleStrikeThrough()
```


## أمثلة



يُظهر كيفية إضافة خط شطب إلى النص.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto para = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Text with a single-line strikethrough.");
run->get_Font()->set_StrikeThrough(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

para = System::ExplicitCast<Aspose::Words::Paragraph>(para->get_ParentNode()->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));

run = System::MakeObject<Aspose::Words::Run>(doc, u"Text with a double-line strikethrough.");
run->get_Font()->set_DoubleStrikeThrough(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Font.StrikeThrough.docx");
```

## انظر أيضًا

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
