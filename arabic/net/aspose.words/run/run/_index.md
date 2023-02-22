---
title: Run.Run
second_title: Aspose.Words لمراجع .NET API
description: Run البناء. يقوم بتهيئة مثيل جديد لملف يجري فئة .
type: docs
weight: 10
url: /ar/net/aspose.words/run/run/
---
## Run(DocumentBase) {#constructor}

يقوم بتهيئة مثيل جديد لملف **يجري** فئة .

```csharp
public Run(DocumentBase doc)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| doc | DocumentBase | وثيقة المالك. |

### ملاحظات

متي **يجري** تم إنشاؤه ، فهو ينتمي إلى المستند المحدد ، ولكنه ليس بعد جزءًا من المستند و **عقدة الأم** باطل.

لإلحاق **يجري** إلى المستند ، استخدم InsertAfter أو InsertBefore في الفقرة التي تريد إدراجها فيها.

### أمثلة

يوضح كيفية إنشاء مستند Aspose.Words يدويًا.

```csharp
Document doc = new Document();

// يحتوي المستند الفارغ على قسم واحد وجسم واحد وفقرة واحدة.
// اتصل بطريقة "RemoveAllChildren" لإزالة كل هذه العقد ،
// وتنتهي بعقدة مستند بدون توابع.
doc.RemoveAllChildren();

// لا يحتوي هذا المستند الآن على عقد فرعية مركبة يمكننا إضافة محتوى إليها.
// إذا كنا نرغب في تعديله ، فسنحتاج إلى إعادة ملء مجموعة العقد الخاصة به.
// أولاً ، قم بإنشاء قسم جديد ، ثم قم بإلحاقه كعقدة فرعية بصفته فرعيًا.
Section section = new Section(doc);
doc.AppendChild(section);

// تعيين بعض خصائص إعداد الصفحة للقسم.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// يحتاج القسم إلى جسم يحتوي على جميع محتوياته ويعرضها
// في الصفحة الواقعة بين رأس وتذييل القسم.
Body body = new Body(doc);
section.AppendChild(body);

// قم بإنشاء فقرة ، وقم بتعيين بعض خصائص التنسيق ، ثم قم بإلحاقها كطفل بالجسم.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// أخيرًا ، أضف بعض المحتوى لعمل المستند. إنشاء شوط ،
// قم بتعيين مظهرها ومحتوياتها ، ثم قم بإلحاقها كطفل بالفقرة.
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
* مساحة الاسم [Aspose.Words](../../run/)
* المجسم [Aspose.Words](../../../)

---

## Run(DocumentBase, string) {#constructor_1}

يقوم بتهيئة مثيل جديد لملف **يجري** فئة .

```csharp
public Run(DocumentBase doc, string text)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| doc | DocumentBase | وثيقة المالك. |
| text | String | نص المدى. |

### ملاحظات

متي **يجري** تم إنشاؤه ، فهو ينتمي إلى المستند المحدد ، ولكنه ليس بعد جزءًا من المستند و **عقدة الأم** باطل.

لإلحاق **يجري** إلى المستند ، استخدم InsertAfter أو InsertBefore في الفقرة التي تريد إدراجها فيها.

### أمثلة

يوضح كيفية تنسيق مجموعة من النص باستخدام خاصية الخط الخاصة به.

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
* مساحة الاسم [Aspose.Words](../../run/)
* المجسم [Aspose.Words](../../../)


