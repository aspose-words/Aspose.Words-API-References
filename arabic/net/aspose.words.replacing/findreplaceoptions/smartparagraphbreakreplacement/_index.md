---
title: FindReplaceOptions.SmartParagraphBreakReplacement
linktitle: SmartParagraphBreakReplacement
articleTitle: SmartParagraphBreakReplacement
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية SmartParagraphBreakReplacement في FindReplaceOptions. تحكّم بسهولة في فواصل الفقرات لتنسيق نصّ سلس.
type: docs
weight: 170
url: /ar/net/aspose.words.replacing/findreplaceoptions/smartparagraphbreakreplacement/
---
## FindReplaceOptions.SmartParagraphBreakReplacement property

يحصل على قيمة منطقية أو يعينها تشير إلى أنه مسموح له باستبدال الفقرة break عندما لا تكون هناك فقرة شقيقة تالية.

القيمة الافتراضية هي`خطأ شنيع`.

```csharp
public bool SmartParagraphBreakReplacement { get; set; }
```

## ملاحظات

يسمح لك هذا الخيار باستبدال فاصل الفقرة عندما لا توجد فقرة شقيقة تالية يمكن نقل جميع عقد child إليها، وذلك من خلال العثور على أي فقرة تالية (ليس بالضرورة شقيقة) بعد الفقرة التي يتم استبدالها.

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
// عندما يتم تعيين الخيار التالي على "true"، سيقوم Aspose.Words بإزالة نص الفقرة
// تمامًا مع علامة الفقرة. وإلا، فسيُحاكي Aspose.Words وورد ويزيل
// نص الفقرة فقط ويترك علامة الفقرة سليمة (عندما يتبع الجدول النص).
options.SmartParagraphBreakReplacement = isSmartParagraphBreakReplacement;
doc.Range.Replace(new Regex(@"TEXT1&p"), "", options);

doc.Save(ArtifactsDir + "Table.RemoveParagraphTextAndMark.docx");
```

### أنظر أيضا

* class [FindReplaceOptions](../)
* مساحة الاسم [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* المجسم [Aspose.Words](../../../)
