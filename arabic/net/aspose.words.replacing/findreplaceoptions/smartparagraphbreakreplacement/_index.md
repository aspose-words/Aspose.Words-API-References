---
title: FindReplaceOptions.SmartParagraphBreakReplacement
linktitle: SmartParagraphBreakReplacement
articleTitle: SmartParagraphBreakReplacement
second_title: Aspose.Words لـ .NET
description: FindReplaceOptions SmartParagraphBreakReplacement ملكية. الحصول على قيمة منطقية أو تعيينها تشير إلى أنه مسموح باستبدال الفقرة Break عندما لا تكون هناك فقرة شقيقة تالية في C#.
type: docs
weight: 160
url: /ar/net/aspose.words.replacing/findreplaceoptions/smartparagraphbreakreplacement/
---
## FindReplaceOptions.SmartParagraphBreakReplacement property

الحصول على قيمة منطقية أو تعيينها تشير إلى أنه مسموح باستبدال الفقرة Break عندما لا تكون هناك فقرة شقيقة تالية.

القيمة الافتراضية هي`خطأ شنيع`.

```csharp
public bool SmartParagraphBreakReplacement { get; set; }
```

## ملاحظات

يسمح هذا الخيار باستبدال فاصل الفقرة في حالة عدم وجود فقرة فرعية تالية يمكن نقل جميع العقد التابعة لها، وذلك من خلال البحث عن أي فقرة تالية (ليست بالضرورة فرعية) بعد الفقرة التي يتم استبدالها.

## أمثلة

يوضح كيفية إزالة فقرة من خلية جدول تحتوي على جدول متداخل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إنشاء جدول يحتوي على فقرة وجدول داخلي في الخلية الأولى.
builder.StartTable();
builder.InsertCell();
builder.Write("TEXT1");
builder.StartTable();
builder.InsertCell();
builder.EndTable();
builder.EndTable();
builder.Writeln();

FindReplaceOptions options = new FindReplaceOptions();
// عندما يتم تعيين الخيار التالي على "صحيح"، سيقوم Aspose.Words بإزالة نص الفقرة
// بالكامل مع علامة الفقرة الخاصة به. وإلا، فإن Aspose.Words سوف يحاكي Word ويزيله
// نص الفقرة فقط ويترك علامة الفقرة سليمة (عندما يتبع الجدول النص).
options.SmartParagraphBreakReplacement = isSmartParagraphBreakReplacement;
doc.Range.Replace(new Regex(@"TEXT1&p"), "", options);

doc.Save(ArtifactsDir + "Table.RemoveParagraphTextAndMark.docx");
```

### أنظر أيضا

* class [FindReplaceOptions](../)
* مساحة الاسم [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* المجسم [Aspose.Words](../../../)
