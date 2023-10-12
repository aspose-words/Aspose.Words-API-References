---
title: TxtLoadOptions.DetectNumberingWithWhitespaces
second_title: Aspose.Words لمراجع .NET API
description: TxtLoadOptions ملكية. يسمح بتحديد كيفية التعرف على عناصر القائمة المرقمة عند استيراد المستند من تنسيق نص عادي. القيمة الافتراضية هيحقيقي.
type: docs
weight: 40
url: /ar/net/aspose.words.loading/txtloadoptions/detectnumberingwithwhitespaces/
---
## TxtLoadOptions.DetectNumberingWithWhitespaces property

يسمح بتحديد كيفية التعرف على عناصر القائمة المرقمة عند استيراد المستند من تنسيق نص عادي. القيمة الافتراضية هي`حقيقي`.

```csharp
public bool DetectNumberingWithWhitespaces { get; set; }
```

### ملاحظات

إذا تم ضبط هذا الخيار على`خطأ شنيع`، تكتشف خوارزمية التعرف على القوائم فقرات القائمة، عندما تنتهي أرقام القائمة بـ إما نقطة أو قوس أيمن أو رموز نقطية (مثل "•" أو "*" أو "-" أو "o").

إذا تم ضبط هذا الخيار على`حقيقي`، يتم استخدام المسافات البيضاء أيضًا كمحددات لأرقام القائمة: خوارزمية التعرف على القائمة لترقيم النمط العربي (1.، 1.1.2.) تستخدم كلاً من المسافات البيضاء ورموز النقطة (".).

### أمثلة

يوضح كيفية اكتشاف القوائم عند تحميل مستندات النص العادي.

```csharp
// قم بإنشاء مستند نص عادي في سلسلة مكونة من أربعة أجزاء منفصلة يمكن تفسيرها على شكل قوائم،
// بمحددات مختلفة. عند تحميل مستند النص العادي إلى كائن "المستند"،
// Aspose.Words سيكتشف دائمًا القوائم الثلاث الأولى وسيضيف كائن "قائمة".
// لكل خاصية "القوائم" في المستند.
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

// قم بإنشاء كائن "TxtLoadOptions"، والذي يمكننا تمريره إلى مُنشئ المستند
// لتعديل كيفية تحميل مستند نص عادي.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// قم بتعيين خاصية "DetectNumberingWithWhitespaces" على "true" للكشف عن العناصر المرقمة
// مع محددات المسافات البيضاء، مثل القائمة الرابعة في وثيقتنا، كقوائم.
// قد يؤدي هذا أيضًا إلى اكتشاف الفقرات التي تبدأ بأرقام كقوائم بشكل خاطئ.
// اضبط خاصية "DetectNumberingWithWhitespaces" على "خطأ"
// لعدم إنشاء قوائم من عناصر مرقمة بمحددات المسافات البيضاء.
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
* مساحة الاسم [Aspose.Words.Loading](../../txtloadoptions/)
* المجسم [Aspose.Words](../../../)


