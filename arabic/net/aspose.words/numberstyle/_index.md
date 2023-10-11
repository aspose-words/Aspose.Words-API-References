---
title: Enum NumberStyle
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.NumberStyle تعداد. يحدد نمط الأرقام للقائمة والحواشي السفلية والتعليقات الختامية وأرقام الصفحات.
type: docs
weight: 4310
url: /ar/net/aspose.words/numberstyle/
---
## NumberStyle enumeration

يحدد نمط الأرقام للقائمة والحواشي السفلية والتعليقات الختامية وأرقام الصفحات.

```csharp
public enum NumberStyle
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Arabic | `0` | الترقيم العربي (1، 2، 3، ...) |
| UppercaseRoman | `1` | الأحرف الكبيرة الرومانية (I، II، III، ...) |
| LowercaseRoman | `2` | الأحرف اللاتينية الصغيرة (i، ii، iii، ...) |
| UppercaseLetter | `3` | الحرف الكبير (A، B، C، ...) |
| LowercaseLetter | `4` | الحروف الصغيرة (أ، ب، ج، ...) |
| Ordinal | `5` | الترتيبي (الأول، الثاني، الثالث، ...) |
| Number | `6` | مرقمة (واحد، اثنان، ثلاثة، ...) |
| OrdinalText | `7` | الترتيبي (النص) (الأول، الثاني، الثالث، ...) |
| Hex | `8` | سداسي عشري: 8، 9، A، B، C، D، E، F، 10، 11، 12 |
| ChicagoManual | `9` | دليل شيكاغو للأسلوب: *، †، † |
| Kanji | `10` | إيديوغراف-رقمي |
| KanjiDigit | `11` | العد الياباني |
| AiueoHalfWidth | `12` | أيويو |
| IrohaHalfWidth | `13` | إيروها |
| ArabicFullWidth | `14` | اللغة العربية كاملة العرض: 1، 2، 3، 4 |
| ArabicHalfWidth | `15` | العربية بنصف العرض: 1، 2، 3، 4 |
| KanjiTraditional | `16` | قانوني ياباني |
| KanjiTraditional2 | `17` | عشرة آلاف رقمي ياباني |
| NumberInCircle | `18` | الدوائر المغلقة |
| DecimalFullWidth | `19` | العرض الكامل العشري: 1، 2، 3، 4 |
| Aiueo | `20` | Aiueo عرض كامل |
| Iroha | `21` | إيروها بالعرض الكامل |
| LeadingZero | `22` | الصفر البادئ (01، 02،...، 09، 10، 11،...، 99، 100، 101،...) |
| Bullet | `23` | تعداد نقطي (تحقق من رمز الحرف في النص) |
| Ganada | `24` | الغاندا الكورية |
| Chosung | `25` | كوريا تشوسونج |
| GB1 | `26` | توقف كامل مغلق |
| GB2 | `27` | الأقواس المغلقة |
| GB3 | `28` | دائرة مغلقة صينية |
| GB4 | `29` | إيديوغراف دائرة مغلقة |
| Zodiac1 | `30` | إيديوغراف تقليدي |
| Zodiac2 | `31` | إيديوغراف زودياك |
| Zodiac3 | `32` | إيديوغراف زودياك تقليدي |
| TradChinNum1 | `33` | العد التايواني |
| TradChinNum2 | `34` | إيديوغراف قانوني تقليدي |
| TradChinNum3 | `35` | العد التايواني ألف |
| TradChinNum4 | `36` | رقمي تايواني |
| SimpChinNum1 | `37` | العد الصيني |
| SimpChinNum2 | `38` | القانون الصيني المبسط |
| SimpChinNum3 | `39` | العد الصيني بالألف |
| SimpChinNum4 | `40` | الصينية (غير منفذة) |
| HanjaRead | `41` | الرقمي الكوري |
| HanjaReadDigit | `42` | العد الكوري |
| Hangul | `43` | قانوني كوريا |
| Hanja | `44` | كوريا الرقمية2 |
| Hebrew1 | `45` | العبرية-1 |
| Arabic1 | `46` | الحروف العربية |
| Hebrew2 | `47` | العبرية-2 |
| Arabic2 | `48` | ابجد عربي |
| HindiLetter1 | `49` | حروف العلة الهندية |
| HindiLetter2 | `50` | الحروف الساكنة الهندية |
| HindiArabic | `51` | الأرقام الهندية |
| HindiCardinalText | `52` | وصفي هندي (كرادلة) |
| ThaiLetter | `53` | الحروف التايلاندية |
| ThaiArabic | `54` | الأرقام التايلاندية |
| ThaiCardinalText | `55` | الوصف التايلاندي (الكرادلة) |
| VietCardinalText | `56` | الوصف الفيتنامي (الكرادلة) |
| NumberInDash | `57` | تنسيق رقم الصفحة: - 1 -، - 2 -، - 3 -، - 4 - |
| LowercaseRussian | `58` | الأبجدية الروسية الصغيرة |
| UppercaseRussian | `59` | الأبجدية الروسية الكبيرة |
| None | `255` | لا يوجد رمز نقطي أو رقم. |
| Custom | `65280` | تنسيق الأرقام المخصص. وهو مدعوم بتنسيق DOCX فقط. |

### أمثلة

يوضح كيفية تطبيق تنسيق القائمة المخصصة على الفقرات عند استخدام DocumentBuilder.

```csharp
Document doc = new Document();

// تسمح لنا القائمة بتنظيم وتزيين مجموعات من الفقرات برموز البادئة والمسافات البادئة.
 // يمكننا إنشاء قوائم متداخلة عن طريق زيادة مستوى المسافة البادئة.
 // يمكننا بدء القائمة وإنهائها باستخدام خاصية "ListFormat" الخاصة بمنشئ المستندات.
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
// أنشئ قائمة من قالب Microsoft Word، وقم بتخصيص المستويين الأولين من قائمتها.
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

// ستعمل قيمة NumberFormat هذه على إنشاء رموز قائمة نقطية على شكل نجمة.
listLevel.NumberFormat = "\xf0af";
listLevel.TrailingCharacter = ListTrailingCharacter.Space;
listLevel.NumberPosition = 144;

// قم بإنشاء فقرات وتطبيق كلا مستويي القائمة بتنسيق القائمة المخصص لدينا عليها.
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


