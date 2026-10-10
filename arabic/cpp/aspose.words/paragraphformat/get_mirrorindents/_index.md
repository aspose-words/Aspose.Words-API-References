---
title: "Aspose::Words::ParagraphFormat::get_MirrorIndents طريقة"
linktitle: "get_MirrorIndents"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::ParagraphFormat::get_MirrorIndents method. يحصل أو يضبط علامة تشير إلى ما إذا كانت الهوامش اليسرى واليمنى ذات عرض متساوٍ في C++."
type: docs
weight: 24500
url: /ar/cpp/aspose.words/paragraphformat/get_mirrorindents/
---
## ParagraphFormat::get_MirrorIndents method


يحصل أو يضبط علامة تشير إلى ما إذا كانت المسافات البادئة اليسرى واليمنى ذات عرض متساوٍ.

```cpp
bool Aspose::Words::ParagraphFormat::get_MirrorIndents()
```


## أمثلة



أظهر كيفية جعل الهوامش اليسرى واليمنى متساوية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat();

format->set_MirrorIndents(true);

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.MirrorIndents.docx");
```

## انظر أيضًا

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
