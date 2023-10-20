---
title: ParagraphFormat.SpaceAfterAuto
linktitle: SpaceAfterAuto
articleTitle: SpaceAfterAuto
second_title: Aspose.Words لـ .NET
description: ParagraphFormat SpaceAfterAuto ملكية. صحيح إذا تم ضبط مقدار التباعد بعد الفقرة تلقائيًا في C#.
type: docs
weight: 310
url: /ar/net/aspose.words/paragraphformat/spaceafterauto/
---
## ParagraphFormat.SpaceAfterAuto property

صحيح إذا تم ضبط مقدار التباعد بعد الفقرة تلقائيًا.

```csharp
public bool SpaceAfterAuto { get; set; }
```

## ملاحظات

عند التعيين على`حقيقي` ، يتجاوز تأثير[`SpaceAfter`](../spaceafter/).

عندما تقوم بتعيين المسافة قبل المسافة للفقرة والمسافة بعدها على تلقائي، يقوم Microsoft Word بإضافة 14 نقطة تباعد بين الفقرات تلقائيًا وفقًا للقواعد التالية:

* عادة، تتم إضافة التباعد بعد كل الفقرات.
* في القائمة ذات التعداد النقطي أو الرقمي، تتم إضافة التباعد فقط بعد العنصر الأخير في القائمة. لا تتم إضافة التباعد بين عناصر القائمة.
* في القائمة المتداخلة ذات التعداد النقطي أو الرقمي، لا تتم إضافة تباعد.
* تتم إضافة التباعد عادة بعد الجدول.
* لا تتم إضافة التباعد بعد الجدول إذا كان هو الكتلة الأخيرة في خلية الجدول.
* لا تتم إضافة التباعد بعد الفقرة الأخيرة في خلية الجدول.

## أمثلة

يوضح كيفية ضبط التباعد التلقائي للفقرات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بتطبيق قدر كبير من التباعد قبل وبعد الفقرات التي سينشئها هذا المنشئ.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// اضبط هذه العلامات على "صحيح" لتطبيق التباعد التلقائي،
// تجاهل التباعد في الخصائص التي حددناها أعلاه بشكل فعال.
// اتركها كـ "خطأ" سيؤدي إلى تطبيق تباعد الفقرات المخصص لدينا.
builder.ParagraphFormat.SpaceAfterAuto = autoSpacing;
builder.ParagraphFormat.SpaceBeforeAuto = autoSpacing;

// أدخل فقرتين بمسافة أعلى وأسفلهما واحفظ المستند.
builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphSpacingAuto.docx");
```

### أنظر أيضا

* class [ParagraphFormat](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
