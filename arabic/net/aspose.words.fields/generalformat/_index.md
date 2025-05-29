---
title: GeneralFormat Enum
linktitle: GeneralFormat
articleTitle: GeneralFormat
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.Fields.GeneralFormat enum، الذي يعزز تنسيق النص الرقمي للحقول، مما يضمن الوضوح والدقة في مستنداتك.
type: docs
weight: 3050
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
| None | `0` | يستخدم لتحديد تنسيق عام مفقود. |
| Aiueo | `1` | تنسيق رقمي. يُنسّق نتيجة رقمية باستخدام أحرف هيراغانا بترتيب aiueo التقليدي. |
| UppercaseAlphabetic | `2` | تنسيق رقمي. يُنسّق النتيجة الرقمية كتكرار واحد أو أكثر لحرف لاتيني أبجدي كبير. |
| LowercaseAlphabetic | `3` | تنسيق رقمي. يُنسّق النتيجة الرقمية كتكرار واحد أو أكثر لحرف لاتيني أبجدي صغير. |
| Arabic | `4` | تنسيق رقمي. تنسيق النتيجة الرقمية باستخدام الأرقام العربية الأصلية. |
| ArabicAbjad | `5` | تنسيق رقمي. يُنسّق النتيجة الرقمية باستخدام أرقام أبجدية تصاعدية. |
| ArabicAlpha | `6` | تنسيق رقمي. يُنسّق النتيجة الرقمية باستخدام الأحرف العربية. |
| ArabicDash | `7` | تنسيق رقمي. يُنسّق النتيجة الرقمية باستخدام الأرقام العربية الأصلية، مع البادئة "-" واللاحقة "-". |
| BahtText | `8` | تنسيق رقمي. يُنسّق نتيجة رقمية بنظام العد التايلاندي. |
| CardText | `9` | تنسيق رقمي. نص أساسي (واحد، اثنان، ثلاثة، ...). |
| ChineseNum1 | `10` | تنسيق رقمي. يُنسّق النتيجة الرقمية باستخدام أرقام تصاعدية من نظام العد المناسب. |
| ChineseNum2 | `11` | تنسيق رقمي. يُنسّق نتيجة رقمية باستخدام أرقام متسلسلة من التنسيق القانوني المناسب. |
| ChineseNum3 | `12` | تنسيق رقمي. يُنسّق نتيجة رقمية باستخدام أرقام متسلسلة من نظام العد بالآلاف المناسب. |
| Chosung | `13` | تنسيق رقمي. يُنسّق نتيجة رقمية باستخدام أرقام متسلسلة من تنسيق تشوسونغ الكوري. |
| CircleNum | `14` | تنسيق رقمي . يُنسّق نتيجة رقمية باستخدام ترقيم عشري مُحاط بدائرة، باستخدام الرمز الأبجدي الرقمي المُحاط للأرقام في النطاق من 1 إلى 20. |
| DBChar | `15` | تنسيق رقمي. يُنسّق النتيجة الرقمية باستخدام ترقيم عربي مزدوج البايت. |
| DBNum1 | `16` | تنسيق رقمي. يُنسّق نتيجة رقمية باستخدام رموز رقمية متسلسلة، باستخدام الحرف المناسب. |
| DBNum2 | `17` | تنسيق رقمي. يُنسّق نتيجة رقمية باستخدام أرقام متسلسلة من نظام العد المناسب. |
| DBNum3 | `18` | تنسيق رقمي. يُنسّق نتيجة رقمية باستخدام أرقام متسلسلة من نظام العد القانوني المناسب. |
| DBNum4 | `19` | تنسيق رقمي. يُنسّق نتيجة رقمية باستخدام أرقام متسلسلة من نظام العد الرقمي المناسب. |
| DollarText | `20` | تنسيق رقمي. نص الدولار (واحد، اثنان، ثلاثة، ... + و٥٥/١٠٠). |
| Ganada | `21` | تنسيق رقمي. يُنسّق نتيجة رقمية باستخدام أرقام متسلسلة من تنسيق غانادا الكوري. |
| GB1 | `22` | تنسيق رقمي. يُنسّق النتيجة الرقمية باستخدام ترقيم عشري متبوع بنقطة، باستخدام الحرف الأبجدي الرقمي المرفق. |
| GB2 | `23` | تنسيق رقمي. يُنسّق النتيجة الرقمية باستخدام ترقيم عشري مُحاط بأقواس، وx000d باستخدام الحرف الأبجدي الرقمي المُحاط. |
| GB3 | `24` | تنسيق رقمي . يُنسّق نتيجة رقمية باستخدام ترقيم عشري مُحاط بدائرة، باستخدام الحرف الأبجدي الرقمي المُحاط بـ . |
| GB4 | `25` | تنسيق رقمي . يُنسّق نتيجة رقمية باستخدام ترقيم عشري مُحاط بدائرة، باستخدام الحرف الأبجدي الرقمي المُحاط بـ . |
| Hebrew1 | `26` | تنسيق رقمي. تنسيق النتيجة الرقمية باستخدام الأرقام العبرية. |
| Hebrew2 | `27` | تنسيق رقمي. يُنسّق النتيجة الرقمية باستخدام الأبجدية العبرية. |
| Hex | `28` | تنسيق رقمي. يُنسّق النتيجة الرقمية باستخدام أرقام سداسية عشرية كبيرة. |
| HindiArabic | `29` | تنسيق رقمي. يُنسّق النتيجة الرقمية باستخدام الأرقام الهندية. |
| HindiCardText | `30` | تنسيق رقمي. يُنسّق نتيجة رقمية باستخدام أرقام متسلسلة من نظام العد الهندي. |
| HindiLetter1 | `31` | تنسيق رقمي. يُنسّق النتيجة الرقمية باستخدام حروف العلة الهندية. |
| HindiLetter2 | `32` | تنسيق رقمي. يُنسّق النتيجة الرقمية باستخدام الحروف الساكنة الهندية. |
| Iroha | `33` | تنسيق رقمي. يُنسّق النتيجة الرقمية باستخدام نظام الإيروها الياباني. |
| KanjiNum1 | `34` | تنسيق رقمي. يُنسّق النتيجة الرقمية باستخدام النمط الياباني باستخدام نظام العد المناسب. |
| KanjiNum2 | `35` | تنسيق رقمي. يُنسّق النتيجة الرقمية باستخدام نظام العد المناسب. |
| KanjiNum3 | `36` | تنسيق رقمي. يُنسّق النتيجة الرقمية باستخدام نظام العد المناسب. |
| Ordinal | `37` | تنسيق رقمي. ترتيبي (الأول، الثاني، الثالث، ...). |
| OrdText | `38` | تنسيق رقمي. نص ترتيبي (الأول، الثاني، الثالث، ...). |
| UppercaseRoman | `39` | تنسيق رقمي. أحرف كبيرة رومانية (I، II، III، ...). |
| LowercaseRoman | `40` | تنسيق رقمي. أحرف رومانية صغيرة (i، ii، iii، ...). |
| SBChar | `41` | تنسيق رقمي. يُنسّق النتيجة الرقمية باستخدام ترقيم عربي أحادي البايت. |
| ThaiArabic | `42` | تنسيق رقمي. يُنسّق النتيجة الرقمية باستخدام الأرقام التايلاندية. |
| ThaiCardText | `43` | تنسيق رقمي. يُنسّق نتيجة رقمية باستخدام أرقام متسلسلة من نظام العد التايلاندي. |
| ThaiLetter | `44` | تنسيق رقمي. يُنسّق النتيجة الرقمية باستخدام الأحرف التايلاندية. |
| VietCardText | `45` | تنسيق رقمي. يُنسّق النتيجة الرقمية باستخدام الأرقام الفيتنامية. |
| Zodiac1 | `46` | تنسيق رقمي. يُنسّق نتيجة رقمية باستخدام رموز رقمية تقليدية متسلسلة. |
| Zodiac2 | `47` | تنسيق رقمي. يُنسّق نتيجة رقمية باستخدام رموز الأبراج المتسلسلة. |
| Zodiac3 | `48` | تنسيق رقمي. يُنسّق نتيجة رقمية باستخدام رموز الأبراج التقليدية المتسلسلة. |
| Caps | `49` | تنسيق النص. كتابة الحرف الأول من كل كلمة بحرف كبير. |
| FirstCap | `50` | تنسيق النص. كتابة الحرف الأول من الكلمة الأولى بحرف كبير. |
| Lower | `51` | تنسيق النص. جميع الأحرف صغيرة. |
| Upper | `52` | تنسيق النص. جميع الأحرف كبيرة. |
| CharFormat | `53` | تنسيق نتيجة الحقل. تعليمة CHARFORMAT. |
| MergeFormat | `54` | تنسيق نتيجة الحقل. تعليمة MERGEFORMAT. |
| MergeFormatInet | `55` | تنسيق نتيجة الحقل. تعليمة MERGEFORMATINET. |

## أمثلة

يوضح كيفية تنسيق نتائج الحقل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// استخدم منشئ المستندات لإدراج حقل يعرض النتيجة دون تطبيق أي تنسيق.
Field field = builder.InsertField("= 2 + 3");

Assert.AreEqual("= 2 + 3", field.GetFieldCode());
Assert.AreEqual("5", field.Result);

//يمكننا تطبيق تنسيق على نتيجة الحقل باستخدام خصائص الحقل.
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

//يمكننا إزالة تنسيقاتنا لإعادة نتيجة الحقل إلى شكلها الأصلي.
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
