---
title: Paragraph
linktitle: Paragraph
articleTitle: Paragraph
second_title: Aspose.Words لـ .NET
description: أنشئ محتوى ديناميكيًا بسهولة باستخدام مُنشئ الفقرات لدينا. هيئ فئة الفقرة الخاصة بك وخصّصها بسهولة لتحسين قابلية القراءة.
type: docs
weight: 10
url: /ar/net/aspose.words/paragraph/paragraph/
---
## Paragraph constructor

يقوم بتهيئة مثيل جديد لـ[`Paragraph`](../) الصف.

```csharp
public Paragraph(DocumentBase doc)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| doc | DocumentBase | وثيقة المالك. |

## ملاحظات

متى[`Paragraph`](../) يتم إنشاؤه، فهو ينتمي إلى المستند المحدد، ولكنه ليس جزءًا من المستند بعد[`ParentNode`](../../node/parentnode/) يكون`باطل`.

لإضافة[`Paragraph`](../) لاستخدام المستند[`InsertAfter`](../../compositenode/insertafter/) أو[`InsertBefore`](../../compositenode/insertbefore/) على القصة التي تريد إدراج الفقرة فيها.

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
* class [Paragraph](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
