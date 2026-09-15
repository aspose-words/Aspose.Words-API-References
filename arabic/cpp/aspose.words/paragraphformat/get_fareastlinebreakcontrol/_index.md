---
title: "طريقة Aspose::Words::ParagraphFormat::get_FarEastLineBreakControl"
linktitle: "get_FarEastLineBreakControl"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::ParagraphFormat::get_FarEastLineBreakControl. يحصل أو يضبط علامة تشير إلى ما إذا كانت قواعد كسر السطر للشرق الأقصى مطبقة على الفقرة الحالية في C++."
type: docs
weight: 12000
url: /ar/cpp/aspose.words/paragraphformat/get_fareastlinebreakcontrol/
---
## ParagraphFormat::get_FarEastLineBreakControl method


يحصل أو يضبط علامة تشير إلى ما إذا كانت قواعد كسر السطر للشرق الآسيوي مطبقة على الفقرة الحالية.

```cpp
bool Aspose::Words::ParagraphFormat::get_FarEastLineBreakControl()
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
