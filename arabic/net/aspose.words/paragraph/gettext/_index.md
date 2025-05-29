---
title: Paragraph.GetText
linktitle: GetText
articleTitle: GetText
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة Paragraph GetText لاسترداد النص بسهولة، بما في ذلك نهايات الفقرات، مما يعزز كفاءة معالجة النصوص لديك.
type: docs
weight: 280
url: /ar/net/aspose.words/paragraph/gettext/
---
## Paragraph.GetText method

يحصل على نص هذه الفقرة بما في ذلك حرف نهاية الفقرة.

```csharp
public override string GetText()
```

## ملاحظات

يتم ربط نصوص جميع العقد الفرعية وإضافة حرف نهاية الفقرة على النحو التالي:

* إذا كانت الفقرة هي الفقرة الأخيرة من[`Body`](../../body/) ، ثم [`SectionBreak`](../../controlchar/sectionbreak/) تمت إضافة (\x000c).
* إذا كانت الفقرة هي الفقرة الأخيرة من[`Cell`](../../../aspose.words.tables/cell/) ، ثم [`Cell`](../../controlchar/cell/) تمت إضافة (\x0007).
* لجميع الفقرات الأخرى [`ParagraphBreak`](../../controlchar/paragraphbreak/) تمت إضافة (\r).

تتضمن السلسلة المرتجعة جميع أحرف التحكم والأحرف الخاصة كما هو موضح في[`ControlChar`](../../controlchar/).

## أمثلة

يوضح كيفية إضافة وتحديث وحذف العقد الفرعية في مجموعة CompositeNode الفرعية.

```csharp
Document doc = new Document();

// تحتوي الوثيقة الفارغة، بشكل افتراضي، على فقرة واحدة.
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// يمكن للعقد المركبة مثل فقرتنا أن تحتوي على عقد مركبة ومضمنة أخرى كأبناء.
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

// إنشاء ثلاث عقد تشغيل أخرى.
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// لن يعرض نص المستند هذه العمليات حتى نقوم بإدخالها في عقدة مركبة
// وهذا في حد ذاته جزء من شجرة عقدة المستند، كما فعلنا في التشغيل الأول.
// يمكننا تحديد مكان محتوى النص للعقد التي نقوم بإدراجها
// يظهر في المستند عن طريق تحديد موقع الإدراج بالنسبة لعقدة أخرى في الفقرة.
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

//أدخل التشغيل الثاني في الفقرة الموجودة أمام التشغيل الأولي.
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

//أدخل التشغيل الثالث بعد التشغيل الأولي.
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

// قم بإدراج التشغيل الأول في بداية مجموعة العقد الفرعية للفقرة.
paragraph.PrependChild(run1);

Assert.AreEqual("Run 1. Run 2. Initial text. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(4, paragraph.GetChildNodes(NodeType.Any, true).Count);

//يمكننا تعديل محتويات التشغيل عن طريق تحرير وحذف العقد الفرعية الموجودة.
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.AreEqual("Run 1. Updated run 2. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, true).Count);
```

### أنظر أيضا

* class [Paragraph](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
