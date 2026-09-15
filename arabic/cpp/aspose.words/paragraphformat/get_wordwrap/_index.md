---
title: "طريقة Aspose::Words::ParagraphFormat::get_WordWrap"
linktitle: "get_WordWrap"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::ParagraphFormat::get_WordWrap. إذا كانت هذه الخاصية خاطئة، يمكن لف النص اللاتيني في وسط كلمة للفقرة الحالية. وإلا يتم لف النص اللاتيني بكلمات كاملة في C++."
type: docs
weight: 42000
url: /ar/cpp/aspose.words/paragraphformat/get_wordwrap/
---
## ParagraphFormat::get_WordWrap method


إذا كانت هذه الخاصية **false**، يمكن لف النص اللاتيني في وسط كلمة للفقرة الحالية. وإلا يتم لف النص اللاتيني بالكلمات الكاملة.

```cpp
bool Aspose::Words::ParagraphFormat::get_WordWrap()
```


## أمثلة



يوضح كيفية تعيين خصائص خاصة للخطوط الآسيوية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat();
format->set_FarEastLineBreakControl(true);
format->set_WordWrap(false);
format->set_HangingPunctuation(true);

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.AsianTypographyProperties.docx");
```

## انظر أيضًا

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
