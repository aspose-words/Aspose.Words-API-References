---
title: Run
linktitle: Run
articleTitle: Run
second_title: Aspose.Words لـ .NET
description: أنشئ وخصّص مثيل فئة Run الخاص بك بسهولة. تمتع بميزات فعّالة لأداء مبسط ووظائف مُحسّنة.
type: docs
weight: 10
url: /ar/net/aspose.words/run/run/
---
## Run(*[DocumentBase](../../documentbase/)*) {#constructor}

يقوم بتهيئة مثيل جديد لـ[`Run`](../) الصف.

```csharp
public Run(DocumentBase doc)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| doc | DocumentBase | وثيقة المالك. |

## ملاحظات

متى[`Run`](../) يتم إنشاؤه، فهو ينتمي إلى المستند المحدد، ولكنه ليس جزءًا من المستند بعد[`ParentNode`](../../node/parentnode/) يكون`باطل`.

لإضافة[`Run`](../) لاستخدام المستند[`InsertAfter`](../../compositenode/insertafter/) أو[`InsertBefore`](../../compositenode/insertbefore/) على الفقرة التي تريد إدراج التشغيل فيها.

## أمثلة

يوضح كيفية إنشاء مستند Aspose.Words يدويًا.

```csharp
Document doc = new Document();

//تحتوي الوثيقة الفارغة على قسم واحد ونص واحد وفقرة واحدة.
//استدعاء طريقة "RemoveAllChildren" لإزالة كل هذه العقد،
// وينتهي الأمر بعقدة مستند بدون أطفال.
doc.RemoveAllChildren();

// لا تحتوي هذه الوثيقة الآن على أي عقد فرعية مركبة يمكننا إضافة محتوى إليها.
// إذا أردنا تحريره، فسوف نحتاج إلى إعادة ملء مجموعة العقد الخاصة به.
// أولاً، قم بإنشاء قسم جديد، ثم قم بإضافته كقسم فرعي إلى عقدة المستند الجذر.
Section section = new Section(doc);
doc.AppendChild(section);

// تعيين بعض خصائص إعداد الصفحة للقسم.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// يحتاج القسم إلى نص، والذي سيحتوي على جميع محتوياته ويعرضها
// على الصفحة بين رأس القسم وتذييله.
Body body = new Body(doc);
section.AppendChild(body);

// قم بإنشاء فقرة، ثم اضبط بعض خصائص التنسيق، ثم أضفها كفقرة فرعية إلى النص.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// أخيرًا، أضف بعض المحتوى لإنشاء المستند. أنشئ مسارًا،
// قم بتعيين مظهره ومحتوياته، ثم قم بإضافته كطفل إلى الفقرة.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### أنظر أيضا

* class [DocumentBase](../../documentbase/)
* class [Run](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## Run(*[DocumentBase](../../documentbase/), string*) {#constructor_1}

يقوم بتهيئة مثيل جديد لـ**يجري** الصف.

```csharp
public Run(DocumentBase doc, string text)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| doc | DocumentBase | وثيقة المالك. |
| text | String | نص الجريدة. |

## ملاحظات

متى[`Run`](../) يتم إنشاؤه، فهو ينتمي إلى المستند المحدد، ولكنه ليس جزءًا من المستند بعد[`ParentNode`](../../node/parentnode/) يكون`باطل`.

لإضافة[`Run`](../) لاستخدام المستند[`InsertAfter`](../../compositenode/insertafter/) أو[`InsertBefore`](../../compositenode/insertbefore/) على الفقرة التي تريد إدراج التشغيل فيها.

## أمثلة

يوضح كيفية تنسيق سلسلة من النص باستخدام خاصية الخط الخاصة به.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

### أنظر أيضا

* class [DocumentBase](../../documentbase/)
* class [Run](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
