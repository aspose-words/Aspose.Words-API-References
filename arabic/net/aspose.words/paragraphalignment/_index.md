---
title: ParagraphAlignment Enum
linktitle: ParagraphAlignment
articleTitle: ParagraphAlignment
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Aspose.Words.ParagraphAlignment لمحاذاة النصوص بدقة في مستنداتك. حسّن سهولة القراءة والتنسيق!
type: docs
weight: 5130
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
| Left | `0` | تم محاذاة النص إلى اليسار. |
| Center | `1` | يتم توسيط النص أفقيًا. |
| Right | `2` | تم محاذاة النص إلى اليمين. |
| Justify | `3` | يتم محاذاة النص إلى اليسار واليمين. |
| Distributed | `4` | يتم توزيع النص بالتساوي. |
| ArabicMediumKashida | `5` | باللغة العربية فقط. طول الكشيدة للنص مُمتد إلى طول متوسط يُحدده المستخدم. |
| ArabicHighKashida | `7` | باللغة العربية فقط. تم تمديد طول الكشيدة للنص إلى أقصى حد ممكن. |
| ArabicLowKashida | `8` | باللغة العربية فقط. تم تمديد طول الكشيدة للنص إلى طول أطول قليلاً. |
| ThaiDistributed | `9` | باللغة التايلاندية فقط. تم محاذاة النص مع تحسين اللغة التايلاندية. |
| MathElementCenterAsGroup | `10` | عنصر الرياضيات الوحيد في السطر، محاذي كـ "مركز كمجموعة". |

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

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
