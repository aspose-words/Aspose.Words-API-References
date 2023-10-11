---
title: Class FindReplaceOptions
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Replacing.FindReplaceOptions فصل. يحدد خيارات عمليات البحث/الاستبدال.
type: docs
weight: 4620
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
| [FindReplaceOptions](findreplaceoptions/#constructor)() | Default_Constructor |
| [FindReplaceOptions](findreplaceoptions/#constructor_1)(FindReplaceDirection) |  |
| [FindReplaceOptions](findreplaceoptions/#constructor_3)(IReplacingCallback) |  |
| [FindReplaceOptions](findreplaceoptions/#constructor_2)(FindReplaceDirection, IReplacingCallback) |  |

## الخصائص

| اسم | وصف |
| --- | --- |
| [ApplyFont](../../aspose.words.replacing/findreplaceoptions/applyfont/) { get; } | تطبيق تنسيق النص على المحتوى الجديد. |
| [ApplyParagraphFormat](../../aspose.words.replacing/findreplaceoptions/applyparagraphformat/) { get; } | تطبيق تنسيق الفقرة على المحتوى الجديد. |
| [Direction](../../aspose.words.replacing/findreplaceoptions/direction/) { get; set; } | تحديد اتجاه الاستبدال. القيمة الافتراضية هيForward . |
| [FindWholeWordsOnly](../../aspose.words.replacing/findreplaceoptions/findwholewordsonly/) { get; set; } | يشير True إلى أن القيمة القديمة يجب أن تكون كلمة مستقلة. |
| [IgnoreDeleted](../../aspose.words.replacing/findreplaceoptions/ignoredeleted/) { get; set; } | الحصول على قيمة منطقية أو تعيينها تشير إما إلى تجاهل النص داخل حذف المراجعات. القيمة الافتراضية هي`خطأ شنيع` . |
| [IgnoreFieldCodes](../../aspose.words.replacing/findreplaceoptions/ignorefieldcodes/) { get; set; } | الحصول على قيمة منطقية أو تعيينها تشير إما إلى تجاهل النص داخل رموز الحقول. القيمة الافتراضية هي`خطأ شنيع` . |
| [IgnoreFields](../../aspose.words.replacing/findreplaceoptions/ignorefields/) { get; set; } | الحصول على قيمة منطقية أو تعيينها للإشارة إلى تجاهل النص الموجود داخل الحقول. القيمة الافتراضية هي`خطأ شنيع` . |
| [IgnoreFootnotes](../../aspose.words.replacing/findreplaceoptions/ignorefootnotes/) { get; set; } | الحصول على قيمة منطقية أو تعيينها للإشارة إلى تجاهل الحواشي السفلية. القيمة الافتراضية هي`خطأ شنيع` . |
| [IgnoreInserted](../../aspose.words.replacing/findreplaceoptions/ignoreinserted/) { get; set; } | الحصول على قيمة منطقية أو تعيينها تشير إما إلى تجاهل النص الموجود داخل مراجعات الإدراج. القيمة الافتراضية هي`خطأ شنيع` . |
| [IgnoreShapes](../../aspose.words.replacing/findreplaceoptions/ignoreshapes/) { get; set; } | الحصول على قيمة منطقية أو تعيينها تشير إلى تجاهل الأشكال داخل النص. |
| [IgnoreStructuredDocumentTags](../../aspose.words.replacing/findreplaceoptions/ignorestructureddocumenttags/) { get; set; } | الحصول على أو تعيين قيمة منطقية تشير إما إلى تجاهل المحتوى[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) . القيمة الافتراضية هي`خطأ شنيع` . |
| [LegacyMode](../../aspose.words.replacing/findreplaceoptions/legacymode/) { get; set; } | الحصول على قيمة منطقية أو تعيينها تشير إلى استخدام خوارزمية البحث/الاستبدال القديمة. |
| [MatchCase](../../aspose.words.replacing/findreplaceoptions/matchcase/) { get; set; } | يشير True إلى مقارنة حساسة لحالة الأحرف، ويشير false إلى مقارنة حساسة لحالة الأحرف. |
| [ReplacingCallback](../../aspose.words.replacing/findreplaceoptions/replacingcallback/) { get; set; } | الطريقة المعرفة من قبل المستخدم والتي يتم استدعاؤها قبل كل حدث استبدال. |
| [SmartParagraphBreakReplacement](../../aspose.words.replacing/findreplaceoptions/smartparagraphbreakreplacement/) { get; set; } | الحصول على قيمة منطقية أو تعيينها تشير إلى أنه مسموح باستبدال الفقرة Break عندما لا تكون هناك فقرة شقيقة تالية. |
| [UseLegacyOrder](../../aspose.words.replacing/findreplaceoptions/uselegacyorder/) { get; set; } | يشير True إلى أن البحث عن النص يتم إجراؤه بشكل تسلسلي من الأعلى إلى الأسفل مع الأخذ في الاعتبار مربعات النص. القيمة الافتراضية هي`خطأ شنيع` . |
| [UseSubstitutions](../../aspose.words.replacing/findreplaceoptions/usesubstitutions/) { get; set; } | الحصول على قيمة منطقية أو تعيينها تشير إلى ما إذا كان سيتم التعرف على البدائل واستخدامها ضمن أنماط الاستبدال. القيمة الافتراضية هي`خطأ شنيع` . |

### أمثلة

يوضح كيفية تبديل حساسية حالة الأحرف عند إجراء عملية البحث والاستبدال.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// يمكننا استخدام كائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
FindReplaceOptions options = new FindReplaceOptions();

// اضبط علامة "MatchCase" على "صحيح" لتطبيق حساسية حالة الأحرف أثناء البحث عن سلاسل لاستبدالها.
// اضبط علامة "MatchCase" على "خطأ" لتجاهل حالة الأحرف أثناء البحث عن نص لاستبداله.
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

يوضح كيفية تبديل عمليات البحث والاستبدال المستقلة للكلمات فقط.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// يمكننا استخدام كائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
FindReplaceOptions options = new FindReplaceOptions();

// اضبط علامة "FindWholeWordsOnly" على "صحيح" لاستبدال النص الذي تم العثور عليه إذا لم يكن جزءًا من كلمة أخرى.
// اضبط علامة "FindWholeWordsOnly" على "خطأ" لاستبدال النص بالكامل بغض النظر عن البيئة المحيطة به.
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Replacing](../../aspose.words.replacing/)
* المجسم [Aspose.Words](../../)


