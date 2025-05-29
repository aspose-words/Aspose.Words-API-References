---
title: ParagraphFormat.SpaceAfterAuto
linktitle: SpaceAfterAuto
articleTitle: SpaceAfterAuto
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ParagraphFormat SpaceAfterAuto. اضبط مسافات الفقرات تلقائيًا للحصول على تصميم مستند أكثر وضوحًا واحترافية.
type: docs
weight: 320
url: /ar/net/aspose.words/paragraphformat/spaceafterauto/
---
## ParagraphFormat.SpaceAfterAuto property

صحيح إذا تم تعيين مقدار المسافة بعد الفقرة تلقائيًا.

```csharp
public bool SpaceAfterAuto { get; set; }
```

## ملاحظات

عند ضبطه على`حقيقي` ، يتجاوز تأثير[`SpaceAfter`](../spaceafter/).

عندما تقوم بتعيين المسافة قبل الفقرة والمسافة بعد إلى تلقائي، يقوم Microsoft Word بإضافة مسافة 14 نقطة بين الفقرات تلقائيًا وفقًا للقواعد التالية:

* عادة، تتم إضافة المسافة بعد كل فقرة.
* في القائمة المرقمة أو المنقطة، تتم إضافة المسافة فقط بعد العنصر الأخير في القائمة. لا تتم إضافة المسافة بين عناصر القائمة.
* في القائمة المتداخلة المرقمة أو المنقطة لا تتم إضافة المسافة.
* يتم عادةً إضافة المسافة بعد الجدول.
* لا تتم إضافة المسافة بعد الجدول إذا كان هو الكتلة الأخيرة في خلية الجدول.
* لا تتم إضافة مسافة بعد الفقرة الأخيرة في خلية الجدول.

## أمثلة

يوضح كيفية تعيين المسافة التلقائية بين الفقرات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بتطبيق قدر كبير من التباعد قبل وبعد الفقرات التي سيقوم هذا المنشئ بإنشائها.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// اضبط هذه العلامات على "صحيح" لتطبيق التباعد التلقائي،
// تجاهل فعليًا التباعد في الخصائص التي حددناها أعلاه.
// تركها على "خطأ" سيؤدي إلى تطبيق المسافة المخصصة للفقرات.
builder.ParagraphFormat.SpaceAfterAuto = autoSpacing;
builder.ParagraphFormat.SpaceBeforeAuto = autoSpacing;

// قم بإدراج فقرتين بحيث يكون هناك مسافة بينهما أعلى وأسفل ثم احفظ المستند.
builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphSpacingAuto.docx");
```

### أنظر أيضا

* class [ParagraphFormat](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
