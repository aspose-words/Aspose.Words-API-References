---
title: "Aspose::Words::NumberStyle enum"
linktitle: "NumberStyle"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::NumberStyle enum. يحدد نمط الرقم للقائمة، الحواشي السفلية والنهائية، أرقام الصفحات في C++."
type: docs
weight: 103000
url: /ar/cpp/aspose.words/numberstyle/
---
## NumberStyle enum


يحدد نمط الأرقام للقائمة، الحواشي السفلية والنهائية، أرقام الصفحات.

```cpp
enum class NumberStyle
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| العربية | 0 | ترقيم عربي (1, 2, 3, ...) |
| UppercaseRoman | 1 | روماني بالحروف الكبيرة (I, II, III, ...) |
| LowercaseRoman | 2 | روماني بالحروف الصغيرة (i, ii, iii, ...) |
| UppercaseLetter | 3 | حرف كبير (A, B, C, ...) |
| LowercaseLetter | 4 | حرف صغير (a, b, c, ...) |
| Ordinal | 5 | ترتيبي (1st, 2nd, 3rd, ...) |
| Number | 6 | مرقّم (One, Two, Three, ...) |
| OrdinalText | 7 | ترتيبي (نص) (First, Second, Third, ...) |
| ست عشري | 8 | ست عشري: 8, 9, A, B, C, D, E, F, 10, 11, 12. |
| ChicagoManual | 9 | دليل شيكاغو لـ [النمط](../style/): *, †, † |
| كانجي | 10 | أيديوغراف-رقمي. |
| KanjiDigit | 11 | العد الياباني. |
| AiueoHalfWidth | 12 | Aiueo. |
| IrohaHalfWidth | 13 | Iroha. |
| ArabicFullWidth | 14 | العربية ذات العرض الكامل: 1, 2, 3, 4. |
| ArabicHalfWidth | 15 | العربية ذات العرض النصف: 1, 2, 3, 4. |
| KanjiTraditional | 16 | القانون الياباني. |
| KanjiTraditional2 | 17 | العشرة آلاف الرقمية اليابانية. |
| NumberInCircle | 18 | دوائر مغلقة. |
| DecimalFullWidth | 19 | العرض الكامل للعدد العشري: 1, 2, 3, 4. |
| Aiueo | 20 | العرض الكامل لـ Aiueo. |
| Iroha | 21 | العرض الكامل لـ Iroha. |
| LeadingZero | 22 | الصفر البادئ (01, 02,..., 09, 10, 11,..., 99, 100, 101,...) |
| Bullet | 23 | نقطة (تحقق من رمز الحرف في النص) |
| Ganada | 24 | غانادا الكورية. |
| Chosung | 25 | كوريا تشوسونغ. |
| GB1 | 26 | نقطة توقف مغلقة. |
| GB2 | 27 | قوس مغلق. |
| GB3 | 28 | دائرة مغلقة صينية. |
| GB4 | 29 | حرف صيني داخل دائرة مغلقة. |
| Zodiac1 | 30 | حرف صيني تقليدي. |
| Zodiac2 | 31 | حرف صيني للبرج. |
| Zodiac3 | 32 | حرف صيني للبرج التقليدي. |
| TradChinNum1 | 33 | العد التايواني. |
| TradChinNum2 | 34 | الأحرف القانونية التقليدية. |
| TradChinNum3 | 35 | العد التايواني بالألف. |
| TradChinNum4 | 36 | الرقمي التايواني. |
| SimpChinNum1 | 37 | العد الصيني. |
| SimpChinNum2 | 38 | الصيني القانوني المبسط. |
| SimpChinNum3 | 39 | العد الصيني بالألف. |
| SimpChinNum4 | 40 | الصيني (غير مُنفّذ) |
| HanjaRead | 41 | الرقمي الكوري. |
| HanjaReadDigit | 42 | العد الكوري. |
| Hangul | 43 | القانون الكوري. |
| Hanja | 44 | كوريا الرقمي2. |
| Hebrew1 | 45 | العبرية-1. |
| Arabic1 | 46 | العربية ألف. |
| Hebrew2 | 47 | العبرية-2. |
| Arabic2 | 48 | العربية أبجد. |
| HindiLetter1 | 49 | حروف العلة الهندية. |
| HindiLetter2 | 50 | حروف الهندية. |
| HindiArabic | 51 | أرقام الهندية. |
| HindiCardinalText | 52 | وصف الهندية (العددية) |
| ThaiLetter | 53 | حروف التايلاندية. |
| ThaiArabic | 54 | أرقام التايلاندية. |
| ThaiCardinalText | 55 | وصف التايلاندية (العددية) |
| VietCardinalText | 56 | وصف الفيتنامية (العددية) |
| NumberInDash | 57 | تنسيق رقم الصفحة: - 1 -، - 2 -، - 3 -، - 4 -. |
| LowercaseRussian | 58 | الأبجدية الروسية بالحروف الصغيرة. |
| الأحرف الكبيرة الروسية | 59 | الأبجدية الروسية بالحروف الكبيرة. |
| None | 255 | بدون نقط أو رقم. |
| مخصص | 65280 | تنسيق رقم مخصص. يتم دعمه فقط في تنسيق DOCX. |


## أمثلة



يوضح كيفية تطبيق تنسيق قائمة مخصص على الفقرات عند استخدام [DocumentBuilder](../documentbuilder/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// تتيح لنا القائمة تنظيم وتزيين مجموعات الفقرات باستخدام رموز البادئة والمسافات البادئة.
// يمكننا إنشاء قوائم متداخلة بزيادة مستوى المسافة البادئة.
// يمكننا بدء وإنهاء قائمة باستخدام خاصية "ListFormat" لكائن Document Builder.
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
// إنشاء قائمة من قالب Microsoft Word، وتخصيص أول مستويين من مستوياتها.
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = list->get_ListLevels()->idx_get(0);
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Red());
listLevel->get_Font()->set_Size(24);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::OrdinalText);
listLevel->set_StartAt(21);
listLevel->set_NumberFormat(u"\x0000");

listLevel->set_NumberPosition(-36);
listLevel->set_TextPosition(144);
listLevel->set_TabPosition(144);

listLevel = list->get_ListLevels()->idx_get(1);
listLevel->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::Bullet);
listLevel->get_Font()->set_Name(u"Wingdings");
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Blue());
listLevel->get_Font()->set_Size(24);

// ستُنشئ قيمة NumberFormat هذه رموز تعداد نقطية على شكل نجمة.
listLevel->set_NumberFormat(u"\xf0af");
listLevel->set_TrailingCharacter(Aspose::Words::Lists::ListTrailingCharacter::Space);
listLevel->set_NumberPosition(144);

// إنشاء فقرات وتطبيق كلا مستويي القائمة من تنسيقنا المخصص علىها.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ListFormat()->set_List(list);
builder->Writeln(u"The quick brown fox...");
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->ListIndent();
builder->Writeln(u"jumped over the lazy dog.");
builder->Writeln(u"jumped over the lazy dog.");

builder->get_ListFormat()->ListOutdent();
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->RemoveNumbers();

builder->get_Document()->Save(get_ArtifactsDir() + u"Lists.CreateCustomList.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
