---
title: "Aspose::Words::ParagraphFormat::get_OutlineLevel طريقة"
linktitle: "get_OutlineLevel"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::ParagraphFormat::get_OutlineLevel طريقة. يحدد مستوى المخطط للفقرة في المستند في C++."
type: docs
weight: 26000
url: /ar/cpp/aspose.words/paragraphformat/get_outlinelevel/
---
## ParagraphFormat::get_OutlineLevel method


يحدد مستوى المخطط للفقرة في المستند.

```cpp
Aspose::Words::OutlineLevel Aspose::Words::ParagraphFormat::get_OutlineLevel()
```


## أمثلة



يوضح كيفية تكوين مستويات التخطيط للفقرة لإنشاء نص قابل للطي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// كل فقرة لها خاصية OutlineLevel، والتي يمكن أن تكون أي رقم من 1 إلى 9، أو القيمة الافتراضية "BodyText".
// ضبط الخاصية على أحد القيم الرقمية سيظهر سهمًا إلى اليسار
// من بداية الفقرة.
builder->get_ParagraphFormat()->set_OutlineLevel(Aspose::Words::OutlineLevel::Level1);
builder->Writeln(u"Paragraph outline level 1.");

// المستوى 1 هو أعلى مستوى. إذا كان هناك فقرة بمستوى أدنى تحت فقرة بمستوى أعلى،
// طي الفقرة ذات المستوى الأعلى سيطوي الفقرة ذات المستوى الأدنى.
builder->get_ParagraphFormat()->set_OutlineLevel(Aspose::Words::OutlineLevel::Level2);
builder->Writeln(u"Paragraph outline level 2.");

// فقرتان من نفس المستوى لن تقوما بطي بعضهما البعض،
// والسهام لا تُطيِّح الفقرات التي تُشير إليها.
builder->get_ParagraphFormat()->set_OutlineLevel(Aspose::Words::OutlineLevel::Level3);
builder->Writeln(u"Paragraph outline level 3.");
builder->Writeln(u"Paragraph outline level 3.");

// القيمة الافتراضية "BodyText" هي الأدنى، والتي يمكن لأي فقرة من أي مستوى أن تُطيِّحها.
builder->get_ParagraphFormat()->set_OutlineLevel(Aspose::Words::OutlineLevel::BodyText);
builder->Writeln(u"Paragraph at main text level.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphOutlineLevel.docx");
```

## انظر أيضًا

* Enum [OutlineLevel](../../outlinelevel/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
