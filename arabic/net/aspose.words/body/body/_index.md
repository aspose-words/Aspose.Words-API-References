---
title: Body
linktitle: Body
articleTitle: Body
second_title: Aspose.Words لـ .NET
description: Body البناء. تهيئة مثيل جديد لـBody فئة في C#.
type: docs
weight: 10
url: /ar/net/aspose.words/body/body/
---
## Body constructor

تهيئة مثيل جديد لـ[`Body`](../) فئة.

```csharp
public Body(DocumentBase doc)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| doc | DocumentBase | وثيقة المالك. |

## ملاحظات

متى[`Body`](../) تم إنشاؤه، فهو ينتمي إلى المستند المحدد، ولكنه ليس بعد جزءًا من المستند و[`ParentNode`](../../node/parentnode/) يكون`باطل`.

لإلحاق[`Body`](../)إلى أ[`Section`](../../section/) يستخدم[`إلحاق الطفل`](../../compositenode/appendchild/)[`أدخل بعد`](../../compositenode/insertafter/) أو[`أدخل قبل`](../../compositenode/insertbefore/) طُرق.

## أمثلة

يوضح كيفية إنشاء مستند Aspose.Words يدويًا.

```csharp
Document doc = new Document();

// يحتوي المستند الفارغ على قسم واحد ونص واحد وفقرة واحدة.
// اتصل بالطريقة "RemoveAllChildren" لإزالة كل تلك العقد،
// وينتهي الأمر بعقدة مستند بدون أطفال.
doc.RemoveAllChildren();

// لا يحتوي هذا المستند الآن على عقد فرعية مركبة يمكننا إضافة محتوى إليها.
// إذا أردنا تعديله، فسنحتاج إلى إعادة ملء مجموعة العقد الخاصة به.
// أولاً، قم بإنشاء قسم جديد، ثم قم بإلحاقه كفرع لعقدة المستند الجذر.
Section section = new Section(doc);
doc.AppendChild(section);

// قم بتعيين بعض خصائص إعداد الصفحة للقسم.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// يحتاج القسم إلى نص يحتوي على جميع محتوياته ويعرضها
// في الصفحة الواقعة بين رأس القسم وتذييله.
Body body = new Body(doc);
section.AppendChild(body);

// أنشئ فقرة، وعيّن بعض خصائص التنسيق، ثم ألحقها كطفل فرعي بالنص.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// وأخيرًا، أضف بعض المحتوى لإجراء المستند. إنشاء تشغيل،
// اضبط مظهرها ومحتوياتها، ثم ألحقها كطفل للفقرة.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### أنظر أيضا

* class [DocumentBase](../../documentbase/)
* class [Body](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
