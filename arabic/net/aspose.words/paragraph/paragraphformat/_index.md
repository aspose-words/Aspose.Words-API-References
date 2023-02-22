---
title: Paragraph.ParagraphFormat
second_title: Aspose.Words لمراجع .NET API
description: Paragraph ملكية. يوفر الوصول إلى خصائص تنسيق الفقرة.
type: docs
weight: 190
url: /ar/net/aspose.words/paragraph/paragraphformat/
---
## Paragraph.ParagraphFormat property

يوفر الوصول إلى خصائص تنسيق الفقرة.

```csharp
public ParagraphFormat ParagraphFormat { get; }
```

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

* class [ParagraphFormat](../../paragraphformat/)
* class [Paragraph](../)
* مساحة الاسم [Aspose.Words](../../paragraph/)
* المجسم [Aspose.Words](../../../)


