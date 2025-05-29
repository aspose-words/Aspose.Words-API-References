---
title: ParagraphFormat.SpaceAfter
linktitle: SpaceAfter
articleTitle: SpaceAfter
second_title: Aspose.Words لـ .NET
description: تحكم في تباعد الفقرات باستخدام خاصية "المسافة بعد". اضبط التباعد بسهولة بالنقاط لتحسين سهولة قراءة مستندك وعرضه.
type: docs
weight: 310
url: /ar/net/aspose.words/paragraphformat/spaceafter/
---
## ParagraphFormat.SpaceAfter property

يحصل على مقدار المسافة (بالنقاط) بعد الفقرة أو يعينه.

```csharp
public double SpaceAfter { get; set; }
```

### استثناءات

| استثناء | حالة |
| --- | --- |
| ArgumentOutOfRangeException | يتم طرحه عندما تكون الحجة خارج نطاق القيم الصالحة. |

## ملاحظات

ليس له تأثير عندما[`SpaceAfterAuto`](../spaceafterauto/) يكون`حقيقي`.

تتراوح القيم الصالحة من 0 إلى 1584 شاملة.

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

يوضح كيفية عدم تطبيق المسافة بين الفقرات بنفس النمط.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بتطبيق قدر كبير من التباعد قبل وبعد الفقرات التي سيقوم هذا المنشئ بإنشائها.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// اضبط علامة "NoSpaceBetweenParagraphsOfSameStyle" على "true" لتطبيقها
// لا توجد مسافة بين الفقرات التي لها نفس النمط، مما سيؤدي إلى تجميع الفقرات المتشابهة.
// اترك علامة "NoSpaceBetweenParagraphsOfSameStyle" على "false"
// لتطبيق التباعد بالتساوي على كل فقرة.
builder.ParagraphFormat.NoSpaceBetweenParagraphsOfSameStyle = noSpaceBetweenParagraphsOfSameStyle;

builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.ParagraphFormat.Style = doc.Styles["Quote"];
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphSpacingSameStyle.docx");
```

### أنظر أيضا

* class [ParagraphFormat](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
