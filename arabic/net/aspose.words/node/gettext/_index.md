---
title: Node.GetText
linktitle: GetText
articleTitle: GetText
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة Node GetText لاسترداد النص بسهولة من العقدة وعناصرها الفرعية، مما يعزز إدارة البيانات وكفاءة التطوير.
type: docs
weight: 120
url: /ar/net/aspose.words/node/gettext/
---
## Node.GetText method

يحصل على نص هذه العقدة وجميع أبنائها.

```csharp
public virtual string GetText()
```

## ملاحظات

تتضمن السلسلة المرتجعة جميع أحرف التحكم والأحرف الخاصة كما هو موضح في[`ControlChar`](../../controlchar/).

## أمثلة

يوضح كيفية استخدام أحرف التحكم.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إدراج فقرات تحتوي على نص باستخدام DocumentBuilder.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// يؤدي تحويل المستند إلى نموذج نصي إلى إظهار أن أحرف التحكم
// تمثل بعض العناصر الهيكلية للمستند، مثل فواصل الصفحات.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                $"Hello again!{ControlChar.Cr}" +
                ControlChar.PageBreak, doc.GetText());

// عند تحويل مستند إلى شكل سلسلة،
// يمكننا حذف بعض أحرف التحكم باستخدام طريقة Trim.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                "Hello again!", doc.GetText().Trim());
```

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

* class [Node](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
