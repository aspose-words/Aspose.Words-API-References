---
title: FindReplaceOptions
second_title: Aspose.Words لمراجع .NET API
description: يحدد خيارات عمليات البحث / الاستبدال.
type: docs
weight: 4360
url: /ar/net/aspose.words.replacing/findreplaceoptions/
---
## FindReplaceOptions class

يحدد خيارات عمليات البحث / الاستبدال.

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
| [ApplyParagraphFormat](../../aspose.words.replacing/findreplaceoptions/applyparagraphformat/) { get; } | تم تطبيق تنسيق الفقرة على المحتوى الجديد. |
| [Direction](../../aspose.words.replacing/findreplaceoptions/direction/) { get; set; } | يحدد اتجاه الاستبدال. القيمة الافتراضية هيForward . |
| [FindWholeWordsOnly](../../aspose.words.replacing/findreplaceoptions/findwholewordsonly/) { get; set; } | صحيح يشير إلى أن oldValue يجب أن تكون كلمة قائمة بذاتها. |
| [IgnoreDeleted](../../aspose.words.replacing/findreplaceoptions/ignoredeleted/) { get; set; } | الحصول على أو تعيين قيمة منطقية تشير إما إلى تجاهل النص داخل مراجعات حذف . القيمة الافتراضية هي`خاطئة` . |
| [IgnoreFieldCodes](../../aspose.words.replacing/findreplaceoptions/ignorefieldcodes/) { get; set; } | الحصول على أو تعيين قيمة منطقية تشير إما إلى تجاهل النص داخل رموز الحقول . القيمة الافتراضية هي`خاطئة` . |
| [IgnoreFields](../../aspose.words.replacing/findreplaceoptions/ignorefields/) { get; set; } | الحصول على أو تعيين قيمة منطقية تشير إما إلى تجاهل النص داخل الحقول. القيمة الافتراضية هي`خاطئة` . |
| [IgnoreFootnotes](../../aspose.words.replacing/findreplaceoptions/ignorefootnotes/) { get; set; } | الحصول على أو تعيين قيمة منطقية تشير إما إلى تجاهل الحواشي السفلية . القيمة الافتراضية هي`خاطئة` . |
| [IgnoreInserted](../../aspose.words.replacing/findreplaceoptions/ignoreinserted/) { get; set; } | الحصول على أو تعيين قيمة منطقية تشير إما إلى تجاهل النص داخل مراجعات الإدراج . القيمة الافتراضية هي`خاطئة` . |
| [LegacyMode](../../aspose.words.replacing/findreplaceoptions/legacymode/) { get; set; } | الحصول على أو تعيين قيمة منطقية تشير إلى استخدام خوارزمية البحث / الاستبدال القديمة. |
| [MatchCase](../../aspose.words.replacing/findreplaceoptions/matchcase/) { get; set; } | يشير True إلى مقارنة حساسة لحالة الأحرف ، بينما يشير الخطأ "خطأ" إلى مقارنة غير حساسة لحالة الأحرف. |
| [ReplacingCallback](../../aspose.words.replacing/findreplaceoptions/replacingcallback/) { get; set; } | الطريقة المعرفة من قبل المستخدم والتي يتم استدعاؤها قبل حدوث كل استبدال. |
| [SmartParagraphBreakReplacement](../../aspose.words.replacing/findreplaceoptions/smartparagraphbreakreplacement/) { get; set; } | الحصول على أو تحديد قيمة منطقية تشير إلى أنه يُسمح باستبدال فقرة break في حالة عدم وجود فقرة شقيقة تالية. |
| [UseLegacyOrder](../../aspose.words.replacing/findreplaceoptions/uselegacyorder/) { get; set; } | تشير True إلى أن البحث عن نص يتم إجراؤه بالتتابع من أعلى إلى أسفل مع الأخذ في الاعتبار مربعات النص. القيمة الافتراضية هي false . |
| [UseSubstitutions](../../aspose.words.replacing/findreplaceoptions/usesubstitutions/) { get; set; } | الحصول على أو تعيين قيمة منطقية تشير إلى ما إذا كان سيتم التعرف على البدائل واستخدامها ضمن أنماط الاستبدال.`خاطئة` . |

### أمثلة

يوضح كيفية تبديل حساسية حالة الأحرف عند إجراء عملية البحث والاستبدال.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// يمكننا استخدام كائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
FindReplaceOptions options = new FindReplaceOptions();

// اضبط علامة "MatchCase" على "true" لتطبيق حساسية حالة الأحرف أثناء البحث عن سلاسل لاستبدالها.
// اضبط علامة "MatchCase" على "خطأ" لتجاهل حالة الأحرف أثناء البحث عن نص لاستبداله.
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

يوضح كيفية التبديل بين عمليات البحث والاستبدال المستقلة عن الكلمات فقط.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// يمكننا استخدام كائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
FindReplaceOptions options = new FindReplaceOptions();

// اضبط علامة "FindWholeWordsOnly" على "true" لاستبدال النص الذي تم العثور عليه إذا لم يكن جزءًا من كلمة أخرى.
// اضبط علامة "FindWholeWordsOnly" على "خطأ" لاستبدال كل النص بغض النظر عن ما يحيط به.
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Replacing](../../aspose.words.replacing/)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
