---
title: "تعداد Aspose::Words::OutlineLevel"
linktitle: "OutlineLevel"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "تعداد Aspose::Words::OutlineLevel. يحدد مستوى المخطط لفقرة في المستند في C++."
type: docs
weight: 105000
url: /ar/cpp/aspose.words/outlinelevel/
---
## OutlineLevel enum


يحدد مستوى المخطط لفقرة في المستند.

```cpp
enum class OutlineLevel
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| Level1 | 0 | الفقرة في مستوى المخطط 1 (أعلى مستوى). |
| المستوى2 | 1 | الفقرة في المستوى التخطيطي 2. |
| المستوى3 | 2 | الفقرة في المستوى التخطيطي 3. |
| المستوى4 | 3 | الفقرة في المستوى التخطيطي 4. |
| المستوى5 | 4 | الفقرة في المستوى التخطيطي 5. |
| المستوى6 | 5 | الفقرة في المستوى التخطيطي 6. |
| المستوى7 | 6 | الفقرة في المستوى التخطيطي 7. |
| المستوى8 | 7 | الفقرة في المستوى التخطيطي 8. |
| المستوى9 | 8 | الفقرة في المستوى التخطيطي 9. |
| BodyText | 9 | الفقرة في مستوى النص الرئيسي. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
