---
title: TxtLoadOptions.DetectNumberingWithWhitespaces
linktitle: DetectNumberingWithWhitespaces
articleTitle: DetectNumberingWithWhitespaces
second_title: Aspose.Words لـ .NET
description: قم بتحسين عمليات استيراد المستندات الخاصة بك باستخدام ميزة DetectNumberingWithWhitespaces في TxtLoadOptions، مما يضمن التعرف الدقيق على القوائم المرقمة من النص العادي.
type: docs
weight: 40
url: /ar/net/aspose.words.loading/txtloadoptions/detectnumberingwithwhitespaces/
---
## TxtLoadOptions.DetectNumberingWithWhitespaces property

يسمح بتحديد كيفية التعرف على عناصر القائمة المرقمة عند استيراد المستند من تنسيق نص عادي. القيمة الافتراضية هي`حقيقي`.

```csharp
public bool DetectNumberingWithWhitespaces { get; set; }
```

## ملاحظات

إذا تم تعيين هذا الخيار على`خطأ شنيع`تكتشف خوارزمية التعرف على القوائم فقرات القائمة، عندما تنتهي أرقام القائمة بـ إما بنقطة أو قوس أيمن أو رمز نقطي (مثل "•" أو "*" أو "-" أو "o").

إذا تم تعيين هذا الخيار على`حقيقي`تُستخدم المسافات البيضاء أيضًا كفواصل لأرقام القوائم: تستخدم خوارزمية التعرف على القائمة للترقيم على النمط العربي (1.، 1.1.2.) كلًا من المسافات البيضاء ورموز النقاط (".").

## أمثلة

يوضح كيفية اكتشاف القوائم عند تحميل مستندات النص العادي.

```csharp
// إنشاء مستند نص عادي في سلسلة مكونة من أربعة أجزاء منفصلة يمكننا تفسيرها كقوائم،
// بفواصل مختلفة. عند تحميل مستند النص العادي إلى كائن "مستند"،
// سيكتشف Aspose.Words دائمًا القوائم الثلاث الأولى وسيضيف كائن "قائمة"
// لكل خاصية "القوائم" الموجودة في المستند.
const string textDoc = "Full stop delimiters:\n" +
                       "1. First list item 1\n" +
                       "2. First list item 2\n" +
                       "3. First list item 3\n\n" +
                       "Right bracket delimiters:\n" +
                       "1) Second list item 1\n" +
                       "2) Second list item 2\n" +
                       "3) Second list item 3\n\n" +
                       "Bullet delimiters:\n" +
                       "• Third list item 1\n" +
                       "• Third list item 2\n" +
                       "• Third list item 3\n\n" +
                       "Whitespace delimiters:\n" +
                       "1 Fourth list item 1\n" +
                       "2 Fourth list item 2\n" +
                       "3 Fourth list item 3";

// قم بإنشاء كائن "TxtLoadOptions"، والذي يمكننا تمريره إلى منشئ المستند
// لتعديل كيفية تحميل مستند النص العادي.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// اضبط خاصية "DetectNumberingWithWhitespaces" على "true" لاكتشاف العناصر المرقمة
// مع فواصل المسافات البيضاء، مثل القائمة الرابعة في مستندنا، كقوائم.
// قد يؤدي هذا أيضًا إلى اكتشاف الفقرات التي تبدأ بالأرقام على أنها قوائم بشكل خاطئ.
// اضبط خاصية "DetectNumberingWithWhitespaces" على "false"
// عدم إنشاء قوائم من العناصر المرقمة باستخدام فواصل المسافات البيضاء.
loadOptions.DetectNumberingWithWhitespaces = detectNumberingWithWhitespaces;

Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(textDoc)), loadOptions);

if (detectNumberingWithWhitespaces)
{
    Assert.AreEqual(4, doc.Lists.Count);
    Assert.True(doc.FirstSection.Body.Paragraphs.Any(p => p.GetText().Contains("Fourth list") && ((Paragraph)p).IsListItem));
}
else
{
    Assert.AreEqual(3, doc.Lists.Count);
    Assert.False(doc.FirstSection.Body.Paragraphs.Any(p => p.GetText().Contains("Fourth list") && ((Paragraph)p).IsListItem));
}
```

### أنظر أيضا

* class [TxtLoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)
