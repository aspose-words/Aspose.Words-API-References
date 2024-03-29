---
title: GeneralFormat Enum
linktitle: GeneralFormat
articleTitle: GeneralFormat
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Fields.GeneralFormat تعداد. يحدد تنسيقًا عامًا يتم تطبيقه على نتيجة رقمية أو نصية أو أي حقل. قد يحتوي الحقل على مجموعة من التنسيقات العامة في C#.
type: docs
weight: 2640
url: /ar/net/aspose.words.fields/generalformat/
---
## GeneralFormat enumeration

يحدد تنسيقًا عامًا يتم تطبيقه على نتيجة رقمية أو نصية أو أي حقل. قد يحتوي الحقل على مجموعة من التنسيقات العامة.

```csharp
public enum GeneralFormat
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | يستخدم لتحديد التنسيق العام المفقود. |
| Aiueo | `1` | التنسيق الرقمي. تنسيق نتيجة رقمية باستخدام أحرف هيراغانا بترتيب aiueo التقليدي. |
| UppercaseAlphabetic | `2` | التنسيق الرقمي. يقوم بتنسيق نتيجة رقمية كتكرار واحد أو أكثر لحرف لاتيني أبجدي كبير. |
| LowercaseAlphabetic | `3` | التنسيق الرقمي. يقوم بتنسيق نتيجة رقمية كتكرار واحد أو أكثر لحرف لاتيني أبجدي صغير. |
| Arabic | `4` | التنسيق الرقمي. تنسيق النتيجة الرقمية باستخدام الأرقام الأساسية العربية. |
| ArabicAbjad | `5` | التنسيق الرقمي. تنسيق نتيجة رقمية باستخدام أرقام أبجد التصاعدية. |
| ArabicAlpha | `6` | التنسيق الرقمي. تنسيق نتيجة رقمية باستخدام الحروف الأبجدية العربية. |
| ArabicDash | `7` | التنسيق الرقمي. يقوم بتنسيق نتيجة رقمية باستخدام الأرقام الأساسية العربية، مع البادئة "-" واللاحقة "-". |
| BahtText | `8` | التنسيق الرقمي. تنسيق نتيجة رقمية في نظام العد التايلاندي. |
| CardText | `9` | التنسيق الرقمي. نص أساسي (واحد، اثنان، ثلاثة، ...). |
| ChineseNum1 | `10` | التنسيق الرقمي. يقوم بتنسيق نتيجة رقمية باستخدام أرقام تصاعدية من نظام العد المناسب. |
| ChineseNum2 | `11` | التنسيق الرقمي. تنسيق نتيجة رقمية باستخدام أرقام متسلسلة من التنسيق القانوني المناسب. |
| ChineseNum3 | `12` | التنسيق الرقمي. يقوم بتنسيق نتيجة رقمية باستخدام أرقام متسلسلة من نظام العد المناسب بالألف. |
| Chosung | `13` | التنسيق الرقمي. تنسيق نتيجة رقمية باستخدام أرقام تسلسلية من تنسيق Chosung الكوري. |
| CircleNum | `14` | التنسيق الرقمي. يقوم بتنسيق نتيجة رقمية باستخدام الترقيم العشري المحاط بدائرة، باستخدام الحرف الرسومي الأبجدي الرقمي المضمن للأرقام الموجودة في النطاق من 1 إلى 20. |
| DBChar | `15` | التنسيق الرقمي. تنسيق نتيجة رقمية باستخدام الترقيم العربي مزدوج البايت. |
| DBNum1 | `16` | التنسيق الرقمي. يقوم بتنسيق نتيجة رقمية باستخدام إيدوغرافات رقمية متسلسلة، باستخدام الحرف المناسب. |
| DBNum2 | `17` | التنسيق الرقمي. يقوم بتنسيق نتيجة رقمية باستخدام أرقام تسلسلية من نظام العد المناسب. |
| DBNum3 | `18` | التنسيق الرقمي. تنسيق نتيجة رقمية باستخدام أرقام متسلسلة من نظام العد القانوني المناسب. |
| DBNum4 | `19` | التنسيق الرقمي. تنسيق نتيجة رقمية باستخدام أرقام متسلسلة من نظام العد الرقمي المناسب. |
| DollarText | `20` | التنسيق الرقمي. نص الدولار (واحد، اثنان، ثلاثة، ... + و 55/100). |
| Ganada | `21` | التنسيق الرقمي. تنسيق نتيجة رقمية باستخدام أرقام تسلسلية من تنسيق Ganada الكوري. |
| GB1 | `22` | التنسيق الرقمي. يقوم بتنسيق نتيجة رقمية باستخدام الترقيم العشري متبوعًا بنقطة، وذلك باستخدام الحرف الرسومي الأبجدي الرقمي المرفق. |
| GB2 | `23` | التنسيق الرقمي. يقوم بتنسيق نتيجة رقمية باستخدام الترقيم العشري المحاط بين قوسين، باستخدام الحرف الرسومي الأبجدي الرقمي المضمن. |
| GB3 | `24` | التنسيق الرقمي. يقوم بتنسيق نتيجة رقمية باستخدام الترقيم العشري المحاط بدائرة، باستخدام الحرف الرسومي الأبجدي الرقمي المحاط. |
| GB4 | `25` | التنسيق الرقمي. يقوم بتنسيق نتيجة رقمية باستخدام الترقيم العشري المحاط بدائرة، باستخدام الحرف الرسومي الأبجدي الرقمي المحاط. |
| Hebrew1 | `26` | التنسيق الرقمي. تنسيق نتيجة رقمية باستخدام الأرقام العبرية. |
| Hebrew2 | `27` | التنسيق الرقمي. تنسيق نتيجة رقمية باستخدام الأبجدية العبرية. |
| Hex | `28` | التنسيق الرقمي. تنسيق النتيجة الرقمية باستخدام الأرقام السداسية العشرية الكبيرة. |
| HindiArabic | `29` | التنسيق الرقمي. تنسيق نتيجة رقمية باستخدام الأرقام الهندية. |
| HindiCardText | `30` | التنسيق الرقمي. تنسيق نتيجة رقمية باستخدام أرقام تسلسلية من نظام العد الهندي. |
| HindiLetter1 | `31` | التنسيق الرقمي. تنسيق نتيجة رقمية باستخدام حروف العلة الهندية. |
| HindiLetter2 | `32` | التنسيق الرقمي. تنسيق نتيجة رقمية باستخدام الحروف الساكنة الهندية. |
| Iroha | `33` | التنسيق الرقمي. تنسيق نتيجة رقمية باستخدام iroha اليابانية. |
| KanjiNum1 | `34` | التنسيق الرقمي. تنسيق نتيجة رقمية باستخدام النمط الياباني باستخدام نظام العد المناسب. |
| KanjiNum2 | `35` | التنسيق الرقمي. تنسيق نتيجة رقمية باستخدام نظام العد المناسب. |
| KanjiNum3 | `36` | التنسيق الرقمي. تنسيق نتيجة رقمية باستخدام نظام العد المناسب. |
| Ordinal | `37` | التنسيق الرقمي. الترتيبي (الأول، الثاني، الثالث، ...). |
| OrdText | `38` | التنسيق الرقمي. النص الترتيبي (الأول، الثاني، الثالث، ...). |
| UppercaseRoman | `39` | التنسيق الرقمي. الأحرف الرومانية الكبيرة (I، II، III، ...). |
| LowercaseRoman | `40` | التنسيق الرقمي. الأحرف الرومانية الصغيرة (i، ii، iii، ...). |
| SBChar | `41` | التنسيق الرقمي. تنسيق نتيجة رقمية باستخدام الترقيم العربي أحادي البايت. |
| ThaiArabic | `42` | التنسيق الرقمي. تنسيق نتيجة رقمية باستخدام الأرقام التايلاندية. |
| ThaiCardText | `43` | التنسيق الرقمي. تنسيق نتيجة رقمية باستخدام أرقام تسلسلية من نظام العد التايلاندي. |
| ThaiLetter | `44` | التنسيق الرقمي. تنسيق نتيجة رقمية باستخدام الحروف التايلاندية. |
| VietCardText | `45` | التنسيق الرقمي. تنسيق نتيجة رقمية باستخدام الأرقام الفيتنامية. |
| Zodiac1 | `46` | التنسيق الرقمي. تنسيق نتيجة رقمية باستخدام الأيديوغرافات الرقمية التقليدية المتسلسلة. |
| Zodiac2 | `47` | التنسيق الرقمي. تنسيق نتيجة رقمية باستخدام إيدوغرافات الأبراج المتسلسلة. |
| Zodiac3 | `48` | التنسيق الرقمي. تنسيق نتيجة رقمية باستخدام إيدوغرافات الأبراج التقليدية المتسلسلة. |
| Caps | `49` | تنسيق النص. تكبير الحرف الأول من كل كلمة. |
| FirstCap | `50` | تنسيق النص. تكبير الحرف الأول من الكلمة الأولى. |
| Lower | `51` | تنسيق النص. جميع الحروف صغيرة. |
| Upper | `52` | تنسيق النص. جميع الحروف كبيرة. |
| CharFormat | `53` | تنسيق نتيجة الحقل. تعليمات CHARFORMAT. |
| MergeFormat | `54` | تنسيق نتيجة الحقل. تعليمات MERGEFORMAT. |
| MergeFormatInet | `55` | تنسيق نتيجة الحقل. تعليمات MERGEFORMATINET. |

## أمثلة

يوضح كيفية تنسيق النتائج الميدانية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// استخدم منشئ المستندات لإدراج حقل يعرض نتيجة بدون تطبيق أي تنسيق.
Field field = builder.InsertField("= 2 + 3");

Assert.AreEqual("= 2 + 3", field.GetFieldCode());
Assert.AreEqual("5", field.Result);

// يمكننا تطبيق تنسيق على نتيجة الحقل باستخدام خصائص الحقل.
// فيما يلي ثلاثة أنواع من التنسيقات التي يمكننا تطبيقها على نتيجة الحقل.
// 1 - التنسيق الرقمي:
FieldFormat format = field.Format;
format.NumericFormat = "$###.00";
field.Update();

Assert.AreEqual("= 2 + 3 \\# $###.00", field.GetFieldCode());
Assert.AreEqual("$  5.00", field.Result);

// 2 - تنسيق التاريخ/الوقت:
field = builder.InsertField("DATE");
format = field.Format;
format.DateTimeFormat = "dddd, MMMM dd, yyyy";
field.Update();

Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());
Console.WriteLine($"Today's date, in {format.DateTimeFormat} format:\n\t{field.Result}");

// 3 - التنسيق العام:
field = builder.InsertField("= 25 + 33");
format = field.Format;
format.GeneralFormats.Add(GeneralFormat.LowercaseRoman);
format.GeneralFormats.Add(GeneralFormat.Upper);
field.Update();

int index = 0;
using (IEnumerator<GeneralFormat> generalFormatEnumerator = format.GeneralFormats.GetEnumerator())
    while (generalFormatEnumerator.MoveNext())
        Console.WriteLine($"General format index {index++}: {generalFormatEnumerator.Current}");

Assert.AreEqual("= 25 + 33 \\* roman \\* Upper", field.GetFieldCode());
Assert.AreEqual("LVIII", field.Result);
Assert.AreEqual(2, format.GeneralFormats.Count);
Assert.AreEqual(GeneralFormat.LowercaseRoman, format.GeneralFormats[0]);

// يمكننا إزالة التنسيقات الخاصة بنا لإعادة نتيجة الحقل إلى شكلها الأصلي.
format.GeneralFormats.Remove(GeneralFormat.LowercaseRoman);
format.GeneralFormats.RemoveAt(0);
Assert.AreEqual(0, format.GeneralFormats.Count);
field.Update();

Assert.AreEqual("= 25 + 33  ", field.GetFieldCode());
Assert.AreEqual("58", field.Result);
Assert.AreEqual(0, format.GeneralFormats.Count);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)
