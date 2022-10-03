---
title: NumberStyle
second_title: Aspose.Words لمراجع .NET API
description: يحدد نمط الرقم لقائمة  الحواشي السفلية والتعليقات الختامية  أرقام الصفحات.
type: docs
weight: 4070
url: /ar/net/aspose.words/numberstyle/
---
## NumberStyle enumeration

يحدد نمط الرقم لقائمة ، الحواشي السفلية والتعليقات الختامية ، أرقام الصفحات.

```csharp
public enum NumberStyle
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Arabic | `0` | ترقيم عربي (1، 2، 3، ...) _ |
| UppercaseRoman | `1` | الحالة الرومانية الكبيرة (I ، II ، III ، ...) _ |
| LowercaseRoman | `2` | أحرف رومانية صغيرة (i، ii، iii، ...) _ |
| UppercaseLetter | `3` | الأحرف الكبيرة (أ ، ب ، ج ، ...) _ |
| LowercaseLetter | `4` | حرف صغير (أ ، ب ، ج ، ...) _ |
| Ordinal | `5` | الترتيب الترتيبي (الأول ، الثاني ، الثالث ، ...) _ |
| Number | `6` | مرقمة (واحد ، اثنان ، ثلاثة ، ...) _ |
| OrdinalText | `7` | ترتيبي (نص) (الأول ، الثاني ، الثالث ، ...) _ |
| Hex | `8` | سداسي عشري: 8، 9، A، B، C، D، E، F، 10، 11، 12 |
| ChicagoManual | `9` | دليل شيكاغو للأسلوب: * ، † ، † |
| Kanji | `10` | إيديوغراف-رقمي_ |
| KanjiDigit | `11` | العد الياباني_ |
| AiueoHalfWidth | `12` | Aiueo |
| IrohaHalfWidth | `13` | Iroha |
| ArabicFullWidth | `14` | عربي كامل العرض: 1 ، 2 ، 3 ، 4 |
| ArabicHalfWidth | `15` | نصف عرض عربي: 1 ، 2 ، 3 ، 4 |
| KanjiTraditional | `16` | اليابانية legal |
| KanjiTraditional2 | `17` | عشرة آلاف يابانية رقمية |
| NumberInCircle | `18` | الدوائر المغلقة_ |
| DecimalFullWidth | `19` | عرض عشري كامل: 1 ، 2 ، 3 ، 4 |
| Aiueo | `20` | Aiueo full width |
| Iroha | `21` | Iroha full width |
| LeadingZero | `22` | صفر بادئة (01 ، 02 ، ... ، 09 ، 10 ، 11 ، ... ، 99 ، 100 ، 101 ، ...) _ |
| Bullet | `23` | رمز نقطي (تحقق من رمز الحرف في النص) |
| Ganada | `24` | Ganada الكورية |
| Chosung | `25` | كوريا Chosung |
| GB1 | `26` | توقف كامل مغلق |
| GB2 | `27` | أقواس مغلقة_ |
| GB3 | `28` | الدائرة المغلقة الصينية_ |
| GB4 | `29` | دائرة مرفقة إيديوغراف_ |
| Zodiac1 | `30` | إيديوغر تقليدية_ |
| Zodiac2 | `31` | إيديوغراف زودياك_ |
| Zodiac3 | `32` | إيديوغراف زودياك التقليدية_ |
| TradChinNum1 | `33` | العد التايواني_ |
| TradChinNum2 | `34` | إيديوغر القانونية التقليدية_ |
| TradChinNum3 | `35` | التايوانية العد بالآلاف |
| TradChinNum4 | `36` | التايوانية الرقمية |
| SimpChinNum1 | `37` | العد الصيني_ |
| SimpChinNum2 | `38` | القانون الصيني المبسط_ |
| SimpChinNum3 | `39` | العد الصيني بالآلاف |
| SimpChinNum4 | `40` | الصينية (لم يتم التنفيذ) |
| HanjaRead | `41` | الكورية الرقمية |
| HanjaReadDigit | `42` | العد الكوري_ |
| Hangul | `43` | كوريا legal |
| Hanja | `44` | كوريا رقمي2 |
| Hebrew1 | `45` | عبري -1 |
| Arabic1 | `46` | العربية alpha |
| Hebrew2 | `47` | عبري -2 |
| Arabic2 | `48` | العربية أبجد_ |
| HindiLetter1 | `49` | أحرف العلة الهندية |
| HindiLetter2 | `50` | الحروف الساكنة الهندية |
| HindiArabic | `51` | الأرقام الهندية_ |
| HindiCardinalText | `52` | الوصفية الهندية (الكرادلة) |
| ThaiLetter | `53` | الحروف التايلاندية_ |
| ThaiArabic | `54` | الأرقام التايلاندية |
| ThaiCardinalText | `55` | الوصفي التايلاندي (الكرادلة) |
| VietCardinalText | `56` | وصفية فيتنامية (الكرادلة) |
| NumberInDash | `57` | تنسيق رقم الصفحة: - 1 - ، - 2 - ، - 3 - ، - 4 - |
| LowercaseRussian | `58` | الأبجدية الروسية الصغيرة_ |
| UppercaseRussian | `59` | الأبجدية الروسية الكبيرة_ |
| None | `255` | بدون رمز نقطي أو رقم . |
| Custom | `65280` | تنسيق الأرقام المخصص. وهو مدعوم بتنسيق DOCX فقط. |

### أمثلة

يوضح كيفية تطبيق تنسيق قائمة مخصص على الفقرات عند استخدام DocumentBuilder.

```csharp
Document doc = new Document();

// تسمح لنا القائمة بتنظيم وتزيين مجموعات من الفقرات برموز بادئة ومسافات بادئة.
// يمكننا إنشاء قوائم متداخلة عن طريق زيادة مستوى المسافة البادئة. 
// يمكننا بدء قائمة وإنهائها باستخدام خاصية "تنسيق القائمة" الخاصة بمنشئ المستندات. 
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
// إنشاء قائمة من قالب Microsoft Word ، وتخصيص أول مستويين من القائمة.
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

// ستنشئ قيمة NumberFormat هذه رموز قائمة ذات تعداد نقطي على شكل نجمة.
listLevel.NumberFormat = "\xf0af";
listLevel.TrailingCharacter = ListTrailingCharacter.Space;
listLevel.NumberPosition = 144;

// أنشئ فقرات وقم بتطبيق كلا مستويي القائمة لتنسيق قائمتنا المخصص عليها.
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

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
