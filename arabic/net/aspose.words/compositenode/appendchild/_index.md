---
title: CompositeNode.AppendChild
linktitle: AppendChild
articleTitle: AppendChild
second_title: Aspose.Words لـ .NET
description: CompositeNode AppendChild طريقة. إضافة العقدة المحددة إلى نهاية قائمة العقد التابعة لهذه العقدة في C#.
type: docs
weight: 60
url: /ar/net/aspose.words/compositenode/appendchild/
---
## CompositeNode.AppendChild method

إضافة العقدة المحددة إلى نهاية قائمة العقد التابعة لهذه العقدة.

```csharp
public Node AppendChild(Node newChild)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| newChild | Node | العقدة المراد إضافتها. |

### قيمة الإرجاع

تمت إضافة العقدة.

## ملاحظات

إذا*newChild* موجود بالفعل في الشجرة، تتم إزالته أولاً.

إذا تم إنشاء العقدة التي يتم إدراجها من مستند آخر، فيجب عليك استخدام [`ImportNode`](../../documentbase/importnode/) لاستيراد العقدة إلى المستند الحالي. يمكن بعد ذلك إدراج العقدة المستوردة في المستند الحالي.

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

* class [Node](../../node/)
* class [CompositeNode](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
