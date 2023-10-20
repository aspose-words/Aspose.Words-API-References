---
title: ParagraphFormat.SpaceBefore
linktitle: SpaceBefore
articleTitle: SpaceBefore
second_title: Aspose.Words لـ .NET
description: ParagraphFormat SpaceBefore ملكية. الحصول على أو تعيين مقدار التباعد بالنقاط قبل الفقرة في C#.
type: docs
weight: 320
url: /ar/net/aspose.words/paragraphformat/spacebefore/
---
## ParagraphFormat.SpaceBefore property

الحصول على أو تعيين مقدار التباعد (بالنقاط) قبل الفقرة.

```csharp
public double SpaceBefore { get; set; }
```

### استثناءات

| استثناء | حالة |
| --- | --- |
| ArgumentOutOfRangeException | يتم طرحه عندما تكون الوسيطة خارج نطاق القيم الصالحة. |

## ملاحظات

ليس له أي تأثير عندما[`SpaceBeforeAuto`](../spacebeforeauto/) يكون`حقيقي`.

تتراوح القيم الصالحة من 0 إلى 1584 ضمناً.

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

يوضح كيفية تطبيق عدم وجود مسافات بين الفقرات بنفس النمط.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بتطبيق قدر كبير من التباعد قبل وبعد الفقرات التي سينشئها هذا المنشئ.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// قم بتعيين علامة "NoSpaceBetweenParagraphsOfSameStyle" على "صحيح" للتطبيق
// لا توجد مسافات بين الفقرات ذات النمط نفسه، مما يؤدي إلى تجميع الفقرات المتشابهة.
// اترك علامة "NoSpaceBetweenParagraphsOfSameStyle" على أنها "خطأ"
// لتطبيق المسافات بالتساوي على كل فقرة.
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
