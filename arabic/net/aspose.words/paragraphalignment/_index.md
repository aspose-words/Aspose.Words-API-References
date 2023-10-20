---
title: ParagraphAlignment Enum
linktitle: ParagraphAlignment
articleTitle: ParagraphAlignment
second_title: Aspose.Words لـ .NET
description: Aspose.Words.ParagraphAlignment تعداد. يحدد محاذاة النص في الفقرة في C#.
type: docs
weight: 4400
url: /ar/net/aspose.words/paragraphalignment/
---
## ParagraphAlignment enumeration

يحدد محاذاة النص في الفقرة.

```csharp
public enum ParagraphAlignment
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Left | `0` | تمت محاذاة النص إلى اليسار. |
| Center | `1` | يتم توسيط النص أفقيًا. |
| Right | `2` | تمت محاذاة النص إلى اليمين. |
| Justify | `3` | تتم محاذاة النص إلى اليسار واليمين. |
| Distributed | `4` | النص موزع بالتساوي. |
| ArabicMediumKashida | `5` | اللغة العربية فقط. يتم تمديد طول كشيدة للنص إلى طول متوسط يحدده المستهلك. |
| ArabicHighKashida | `7` | اللغة العربية فقط. يتم تمديد طول الكشيدة للنص إلى أوسع طول ممكن. |
| ArabicLowKashida | `8` | اللغة العربية فقط. تم تمديد طول الكشيدة للنص إلى طول أطول قليلاً. |
| ThaiDistributed | `9` | التايلاندية فقط. تم تبرير النص من خلال تحسين اللغة التايلاندية. |
| MathElementCenterAsGroup | `10` | عنصر الرياضيات الوحيد في السطر، محاذٍ كـ "توسيط كمجموعة". |

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

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
