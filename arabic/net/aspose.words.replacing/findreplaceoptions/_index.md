---
title: FindReplaceOptions Class
linktitle: FindReplaceOptions
articleTitle: FindReplaceOptions
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.FindReplaceOptions للحصول على ميزات البحث والاستبدال المتقدمة، مما يعزز تحرير المستندات بدقة ومرونة.
type: docs
weight: 5350
url: /ar/net/aspose.words.replacing/findreplaceoptions/
---
## FindReplaceOptions class

يحدد خيارات عمليات البحث/الاستبدال.

لمعرفة المزيد، قم بزيارة[البحث والاستبدال](https://docs.aspose.com/words/net/find-and-replace/) مقالة توثيقية.

```csharp
public class FindReplaceOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FindReplaceOptions](findreplaceoptions/#constructor)() | يقوم بتهيئة مثيل جديد لفئة FindReplaceOptions باستخدام الإعدادات الافتراضية. |
| [FindReplaceOptions](findreplaceoptions/#constructor_1)(*[FindReplaceDirection](../findreplacedirection/)*) | يقوم بتهيئة مثيل جديد لفئة FindReplaceOptions بالاتجاه المحدد. |
| [FindReplaceOptions](findreplaceoptions/#constructor_3)(*[IReplacingCallback](../ireplacingcallback/)*) | يقوم بتهيئة مثيل جديد لفئة FindReplaceOptions باستخدام استدعاء الاستبدال المحدد. |
| [FindReplaceOptions](findreplaceoptions/#constructor_2)(*[FindReplaceDirection](../findreplacedirection/), [IReplacingCallback](../ireplacingcallback/)*) | يقوم بتهيئة مثيل جديد لفئة FindReplaceOptions بالاتجاه المحدد واستدعاء الاستبدال. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [ApplyFont](../../aspose.words.replacing/findreplaceoptions/applyfont/) { get; } | تم تطبيق تنسيق النص على المحتوى الجديد. |
| [ApplyParagraphFormat](../../aspose.words.replacing/findreplaceoptions/applyparagraphformat/) { get; } | تم تطبيق تنسيق الفقرة على المحتوى الجديد. |
| [Direction](../../aspose.words.replacing/findreplaceoptions/direction/) { get; set; } | يحدد اتجاه الاستبدال. القيمة الافتراضية هيForward . |
| [FindWholeWordsOnly](../../aspose.words.replacing/findreplaceoptions/findwholewordsonly/) { get; set; } | يشير True إلى أن oldValue يجب أن تكون كلمة مستقلة. |
| [IgnoreDeleted](../../aspose.words.replacing/findreplaceoptions/ignoredeleted/) { get; set; } | يحصل على قيمة منطقية أو يعينها للإشارة إلى تجاهل النص داخل مراجعات الحذف. القيمة الافتراضية هي`خطأ شنيع` . |
| [IgnoreFieldCodes](../../aspose.words.replacing/findreplaceoptions/ignorefieldcodes/) { get; set; } | يحصل على قيمة منطقية أو يعينها للإشارة إلى تجاهل النص داخل أكواد الحقول. القيمة الافتراضية هي`خطأ شنيع` . |
| [IgnoreFields](../../aspose.words.replacing/findreplaceoptions/ignorefields/) { get; set; } | يحصل على قيمة منطقية أو يعينها للإشارة إلى تجاهل النص داخل الحقول. القيمة الافتراضية هي`خطأ شنيع` . |
| [IgnoreFootnotes](../../aspose.words.replacing/findreplaceoptions/ignorefootnotes/) { get; set; } | يحصل على قيمة منطقية أو يعينها للإشارة إلى تجاهل الحواشي السفلية. القيمة الافتراضية هي`خطأ شنيع` . |
| [IgnoreInserted](../../aspose.words.replacing/findreplaceoptions/ignoreinserted/) { get; set; } | يحصل على قيمة منطقية أو يعينها للإشارة إلى تجاهل النص داخل مراجعات الإدراج. القيمة الافتراضية هي`خطأ شنيع` . |
| [IgnoreShapes](../../aspose.words.replacing/findreplaceoptions/ignoreshapes/) { get; set; } | يحصل على قيمة منطقية أو يعينها للإشارة إلى تجاهل الأشكال داخل النص. |
| [IgnoreStructuredDocumentTags](../../aspose.words.replacing/findreplaceoptions/ignorestructureddocumenttags/) { get; set; } | يحصل على قيمة منطقية أو يعينها للإشارة إلى تجاهل محتوى[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) . القيمة الافتراضية هي`خطأ شنيع` . |
| [LegacyMode](../../aspose.words.replacing/findreplaceoptions/legacymode/) { get; set; } | يحصل على قيمة منطقية أو يعينها للإشارة إلى استخدام خوارزمية البحث/الاستبدال القديمة. |
| [MatchCase](../../aspose.words.replacing/findreplaceoptions/matchcase/) { get; set; } | يشير True إلى مقارنة حساسة لحالة الأحرف، ويشير false إلى مقارنة غير حساسة لحالة الأحرف. |
| [ReplacementFormat](../../aspose.words.replacing/findreplaceoptions/replacementformat/) { get; set; } | يُحدد تنسيق الاستبدال. الافتراضي هوText . |
| [ReplacingCallback](../../aspose.words.replacing/findreplaceoptions/replacingcallback/) { get; set; } | الطريقة المحددة من قبل المستخدم والتي يتم استدعاؤها قبل كل عملية استبدال. |
| [SmartParagraphBreakReplacement](../../aspose.words.replacing/findreplaceoptions/smartparagraphbreakreplacement/) { get; set; } | يحصل على قيمة منطقية أو يعينها تشير إلى أنه مسموح له باستبدال الفقرة break عندما لا تكون هناك فقرة شقيقة تالية. |
| [UseLegacyOrder](../../aspose.words.replacing/findreplaceoptions/uselegacyorder/) { get; set; } | يشير True إلى أن البحث عن النص يتم بشكل تسلسلي من الأعلى إلى الأسفل مع مراعاة مربعات النص. القيمة الافتراضية هي`خطأ شنيع` . |
| [UseSubstitutions](../../aspose.words.replacing/findreplaceoptions/usesubstitutions/) { get; set; } | يحصل على قيمة منطقية أو يعينها للإشارة إلى ما إذا كان سيتم التعرف على الاستبدالات واستخدامها داخل أنماط الاستبدال. القيمة الافتراضية هي`خطأ شنيع` . |

## أمثلة

يوضح كيفية تبديل حساسية الحالة عند إجراء عملية البحث والاستبدال.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// يمكننا استخدام الكائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
FindReplaceOptions options = new FindReplaceOptions();

// اضبط علامة "MatchCase" على "true" لتطبيق حساسية الحالة أثناء البحث عن السلاسل التي يجب استبدالها.
// اضبط علامة "MatchCase" على "false" لتجاهل حالة الأحرف أثناء البحث عن نص لاستبداله.
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

يوضح كيفية تبديل عمليات البحث والاستبدال الخاصة بالكلمات المستقلة فقط.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// يمكننا استخدام الكائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
FindReplaceOptions options = new FindReplaceOptions();

// اضبط علامة "FindWholeWordsOnly" على "true" لاستبدال النص الموجود إذا لم يكن جزءًا من كلمة أخرى.
// اضبط علامة "FindWholeWordsOnly" على "false" لاستبدال كل النص بغض النظر عن محيطه.
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Replacing](../../aspose.words.replacing/)
* المجسم [Aspose.Words](../../)
