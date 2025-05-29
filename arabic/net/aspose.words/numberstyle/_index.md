---
title: NumberStyle Enum
linktitle: NumberStyle
articleTitle: NumberStyle
second_title: Aspose.Words لـ .NET
description: اكتشف مجموعة Aspose.Words.NumberStyle لتخصيص أرقام صفحات الحواشي السفلية والختامية، مما يعزز تنسيق مستندك بسهولة.
type: docs
weight: 5040
url: /ar/net/aspose.words/numberstyle/
---
## NumberStyle enumeration

يحدد نمط الأرقام للقائمة والحواشي السفلية والختامية وأرقام الصفحات.

```csharp
public enum NumberStyle
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Arabic | `0` | الترقيم العربي (1، 2، 3، ...) |
| UppercaseRoman | `1` | الأحرف الكبيرة الرومانية (I، II، III، ...) |
| LowercaseRoman | `2` | أحرف رومانية صغيرة (i، ii، iii، ...) |
| UppercaseLetter | `3` | الحرف الكبير (A, B, C, ...) |
| LowercaseLetter | `4` | حرف صغير (a, b, c, ...) |
| Ordinal | `5` | الترتيبي (الأول، الثاني، الثالث، ...) |
| Number | `6` | مرقمة (واحد، اثنان، ثلاثة، ...) |
| OrdinalText | `7` | الترتيب (النص) (الأول، الثاني، الثالث، ...) |
| Hex | `8` | سداسي عشري: 8، 9، أ، ب، ج، د، هـ، و، 10، 11، 12 |
| ChicagoManual | `9` | دليل شيكاغو للأسلوب: *، †، † |
| Kanji | `10` | رسم تخطيطي رقمي |
| KanjiDigit | `11` | العد الياباني |
| AiueoHalfWidth | `12` | أيوو |
| IrohaHalfWidth | `13` | إيروها |
| ArabicFullWidth | `14` | عرض كامل باللغة العربية: 1، 2، 3، 4 |
| ArabicHalfWidth | `15` | نصف العرض العربية: 1، 2، 3، 4 |
| KanjiTraditional | `16` | قانوني ياباني |
| KanjiTraditional2 | `17` | عشرة آلاف يابانية رقمية |
| NumberInCircle | `18` | الدوائر المغلقة |
| DecimalFullWidth | `19` | العرض الكامل العشري: 1، 2، 3، 4 |
| Aiueo | `20` | عرض كامل Aiueo |
| Iroha | `21` | إيروها العرض الكامل |
| LeadingZero | `22` | الصفر الرئيسي (01، 02،...، 09، 10، 11،...، 99، 100، 101،...) |
| Bullet | `23` | رصاصة (تحقق من رمز الحرف في النص) |
| Ganada | `24` | غانادا الكورية |
| Chosung | `25` | كوريا تشوسونغ |
| GB1 | `26` | نقطة مغلقة |
| GB2 | `27` | قوسين مغلقين |
| GB3 | `28` | دائرة مغلقة صينية |
| GB4 | `29` | دائرة مغلقة مرسومة باليد |
| Zodiac1 | `30` | الكتابة اليدوية التقليدية |
| Zodiac2 | `31` | رمز الأبراج |
| Zodiac3 | `32` | رمز الأبراج التقليدي |
| TradChinNum1 | `33` | العد التايواني |
| TradChinNum2 | `34` | إيديوغرام قانوني تقليدي |
| TradChinNum3 | `35` | التايوانيون يعدون الآلاف |
| TradChinNum4 | `36` | تايوانية رقمية |
| SimpChinNum1 | `37` | العد الصيني |
| SimpChinNum2 | `38` | القانون الصيني المبسط |
| SimpChinNum3 | `39` | العد الصيني للألف |
| SimpChinNum4 | `40` | الصينية (غير مطبقة) |
| HanjaRead | `41` | الكورية الرقمية |
| HanjaReadDigit | `42` | العد الكوري |
| Hangul | `43` | كوريا القانونية |
| Hanja | `44` | كوريا الرقمية2 |
| Hebrew1 | `45` | العبرية-1 |
| Arabic1 | `46` | الأبجدية العربية |
| Hebrew2 | `47` | العبرية-2 |
| Arabic2 | `48` | أبجدية عربية |
| HindiLetter1 | `49` | حروف العلة الهندية |
| HindiLetter2 | `50` | الحروف الساكنة الهندية |
| HindiArabic | `51` | أرقام هندية |
| HindiCardinalText | `52` | وصف باللغة الهندية (كاردينالات) |
| ThaiLetter | `53` | الحروف التايلاندية |
| ThaiArabic | `54` | الأرقام التايلاندية |
| ThaiCardinalText | `55` | الوصف التايلاندي (الكرادلة) |
| VietCardinalText | `56` | الوصف الفيتنامي (الكرادلة) |
| NumberInDash | `57` | تنسيق رقم الصفحة: - 1 -، - 2 -، - 3 -، - 4 - |
| LowercaseRussian | `58` | الأبجدية الروسية الصغيرة |
| UppercaseRussian | `59` | الأبجدية الروسية الكبيرة |
| None | `255` | لا يوجد رصاصة أو رقم. |
| Custom | `65280` | تنسيق أرقام مخصص. يدعم تنسيق DOCX فقط. |

## أمثلة

يوضح كيفية تطبيق تنسيق القائمة المخصصة على الفقرات عند استخدام DocumentBuilder.

```csharp
Document doc = new Document();

// تسمح لنا القائمة بتنظيم وتزيين مجموعات من الفقرات باستخدام رموز البادئة والمسافات البادئة.
 //يمكننا إنشاء قوائم متداخلة عن طريق زيادة مستوى المسافة البادئة.
 // يمكننا أن نبدأ وننهي القائمة باستخدام خاصية "ListFormat" الموجودة في منشئ المستندات.
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
// قم بإنشاء قائمة من قالب Microsoft Word، ثم قم بتخصيص المستويين الأولين من القائمة.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

ListLevel listLevel = list.ListLevels[0];
listLevel.Font.Color = Color.Red;
listLevel.Font.Size = 24;
listLevel.NumberStyle = NumberStyle.OrdinalText;
listLevel.StartAt = 21;
listLevel.NumberFormat = "\x0000";

listLevel.NumberPosition = -36;
listLevel.TextPosition = 144;
listLevel.TabPosition = 144;

listLevel = list.ListLevels[1];
listLevel.Alignment = ListLevelAlignment.Right;
listLevel.NumberStyle = NumberStyle.Bullet;
listLevel.Font.Name = "Wingdings";
listLevel.Font.Color = Color.Blue;
listLevel.Font.Size = 24;

// ستقوم قيمة NumberFormat هذه بإنشاء رموز قائمة نقطية على شكل نجمة.
listLevel.NumberFormat = "\xf0af";
listLevel.TrailingCharacter = ListTrailingCharacter.Space;
listLevel.NumberPosition = 144;

// قم بإنشاء فقرات ثم قم بتطبيق مستويي القائمة لتنسيق القائمة المخصصة عليها.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.List = list;
builder.Writeln("The quick brown fox...");
builder.Writeln("The quick brown fox...");

builder.ListFormat.ListIndent();
builder.Writeln("jumped over the lazy dog.");
builder.Writeln("jumped over the lazy dog.");

builder.ListFormat.ListOutdent();
builder.Writeln("The quick brown fox...");

builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateCustomList.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
