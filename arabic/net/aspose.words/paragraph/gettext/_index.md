---
title: Paragraph.GetText
linktitle: GetText
articleTitle: GetText
second_title: Aspose.Words لـ .NET
description: Paragraph GetText طريقة. الحصول على نص هذه الفقرة بما في ذلك حرف نهاية الفقرة في C#.
type: docs
weight: 260
url: /ar/net/aspose.words/paragraph/gettext/
---
## Paragraph.GetText method

الحصول على نص هذه الفقرة بما في ذلك حرف نهاية الفقرة.

```csharp
public override string GetText()
```

## ملاحظات

يتم ربط نص جميع العقد الفرعية ويتم إلحاق حرف نهاية الفقرة على النحو التالي:

* إذا كانت الفقرة هي الفقرة الأخيرة من[`Body`](../../body/) ، ثم [`SectionBreak`](../../controlchar/sectionbreak/) تم إلحاق (\x000c).
* إذا كانت الفقرة هي الفقرة الأخيرة من[`Cell`](../../../aspose.words.tables/cell/) ، ثم [`Cell`](../../controlchar/cell/) تم إلحاق (\x0007).
* لجميع الفقرات الأخرى [`ParagraphBreak`](../../controlchar/paragraphbreak/) (\r) تم إلحاقه.

تتضمن السلسلة التي تم إرجاعها جميع عناصر التحكم والأحرف الخاصة كما هو موضح في[`ControlChar`](../../controlchar/).

## أمثلة

يوضح كيفية إضافة وتحديث وحذف العقد الفرعية في مجموعة CompositeNode الفرعية.

```csharp
Document doc = new Document();

// يحتوي المستند الفارغ افتراضيًا على فقرة واحدة.
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// العقد المركبة مثل فقرتنا يمكن أن تحتوي على عقد مركبة ومضمنة أخرى كأبناء.
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

// أنشئ ثلاث عقد تشغيل أخرى.
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// لن يعرض نص المستند عمليات التشغيل هذه حتى نقوم بإدراجها في عقدة مركبة
// الذي يعد في حد ذاته جزءًا من شجرة عقدة المستند، كما فعلنا مع التشغيل الأول.
// يمكننا تحديد مكان محتويات النص للعقد التي نقوم بإدراجها
// يظهر في المستند عن طريق تحديد موقع الإدراج بالنسبة لعقدة أخرى في الفقرة.
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

// أدخل التشغيل الثاني في الفقرة الموجودة أمام التشغيل الأولي.
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

// أدخل الجولة الثالثة بعد التشغيل الأولي.
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

// أدخل التشغيل الأول في بداية مجموعة العقد الفرعية للفقرة.
paragraph.PrependChild(run1);

Assert.AreEqual("Run 1. Run 2. Initial text. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(4, paragraph.GetChildNodes(NodeType.Any, true).Count);

// يمكننا تعديل محتويات التشغيل عن طريق تحرير وحذف العقد الفرعية الموجودة.
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.AreEqual("Run 1. Updated run 2. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, true).Count);
```

### أنظر أيضا

* class [Paragraph](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
