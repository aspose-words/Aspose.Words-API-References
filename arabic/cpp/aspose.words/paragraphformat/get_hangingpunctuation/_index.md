---
title: "Aspose::Words::ParagraphFormat::get_HangingPunctuation طريقة"
linktitle: "get_HangingPunctuation"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::ParagraphFormat::get_HangingPunctuation طريقة. يحصل على أو يعيّن علامة تشير إلى ما إذا كانت علامات الترقيم المتدلية مفعلة للفقرة الحالية في C++."
type: docs
weight: 14000
url: /ar/cpp/aspose.words/paragraphformat/get_hangingpunctuation/
---
## ParagraphFormat::get_HangingPunctuation method


يحصل أو يضبط علامة تشير إلى ما إذا كانت علامات الترقيم المعلقة مفعلة للفقرة الحالية.

```cpp
bool Aspose::Words::ParagraphFormat::get_HangingPunctuation()
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
