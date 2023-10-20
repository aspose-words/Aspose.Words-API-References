---
title: ImportFormatOptions Class
linktitle: ImportFormatOptions
articleTitle: ImportFormatOptions
second_title: Aspose.Words لـ .NET
description: Aspose.Words.ImportFormatOptions فصل. يسمح بتحديد خيارات الاستيراد المتنوعة لتنسيق الإخراج في C#.
type: docs
weight: 3240
url: /ar/net/aspose.words/importformatoptions/
---
## ImportFormatOptions class

يسمح بتحديد خيارات الاستيراد المتنوعة لتنسيق الإخراج.

لمعرفة المزيد، قم بزيارة[تحديد خيارات التحميل](https://docs.aspose.com/words/net/specify-load-options/) مقالة توثيقية.

```csharp
public class ImportFormatOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [ImportFormatOptions](importformatoptions/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [AdjustSentenceAndWordSpacing](../../aspose.words/importformatoptions/adjustsentenceandwordspacing/) { get; set; } | الحصول على قيمة منطقية أو تعيينها والتي تحدد ما إذا كان سيتم ضبط تباعد الجملة والكلمات تلقائيًا. القيمة الافتراضية هي`خطأ شنيع` . |
| [ForceCopyStyles](../../aspose.words/importformatoptions/forcecopystyles/) { get; set; } | الحصول على قيمة منطقية أو تعيينها تشير إما إلى نسخ الأنماط المتعارضة فيKeepSourceFormatting mode. القيمة الافتراضية هي`خطأ شنيع` . |
| [IgnoreHeaderFooter](../../aspose.words/importformatoptions/ignoreheaderfooter/) { get; set; } | الحصول على أو تعيين قيمة منطقية تحدد تنسيق المصدر لمحتوى الرؤوس/التذييلات الذي تم تجاهله إذاKeepSourceFormatting يتم استخدام الوضع. القيمة الافتراضية هي`حقيقي` . |
| [IgnoreTextBoxes](../../aspose.words/importformatoptions/ignoretextboxes/) { get; set; } | الحصول على أو تعيين قيمة منطقية تحدد تنسيق المصدر لمحتوى مربعات النص الذي تم تجاهله إذاKeepSourceFormatting يتم استخدام الوضع. القيمة الافتراضية هي`حقيقي` . |
| [KeepSourceNumbering](../../aspose.words/importformatoptions/keepsourcenumbering/) { get; set; } | الحصول على قيمة منطقية أو تعيينها والتي تحدد كيفية استيراد الترقيم عندما يتعارض مع مستندات المصدر و الوجهة. القيمة الافتراضية هي`خطأ شنيع` . |
| [MergePastedLists](../../aspose.words/importformatoptions/mergepastedlists/) { get; set; } | الحصول على أو تعيين قيمة منطقية تحدد ما إذا كان سيتم دمج القوائم الملصقة مع القوائم المحيطة. القيمة الافتراضية هي`خطأ شنيع` . |
| [SmartStyleBehavior](../../aspose.words/importformatoptions/smartstylebehavior/) { get; set; } | الحصول على أو تعيين قيمة منطقية تحدد كيفية استيراد الأنماط عندما يكون لها أسماء متساوية في المستندات المصدر والوجهة. القيمة الافتراضية هي`خطأ شنيع` . |

## أمثلة

يوضح كيفية حل الأنماط المكررة أثناء إدراج المستندات.

```csharp
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);

Style myStyle = builder.Document.Styles.Add(StyleType.Paragraph, "MyStyle");
myStyle.Font.Size = 14;
myStyle.Font.Name = "Courier New";
myStyle.Font.Color = Color.Blue;

builder.ParagraphFormat.StyleName = myStyle.Name;
builder.Writeln("Hello world!");

// انسخ المستند وقم بتحرير نمط "MyStyle" الخاص بالمستنسخ، بحيث يكون لونه مختلفًا عن اللون الأصلي.
// إذا قمنا بإدراج النسخة في المستند الأصلي، فسيتسبب النمطان اللذان يحملان نفس الاسم في حدوث تعارض.
Document srcDoc = dstDoc.Clone();
srcDoc.Styles["MyStyle"].Font.Color = Color.Red;

// عندما نقوم بتمكين SmartStyleBehavior ونستخدم وضع تنسيق الاستيراد KeepSourceFormatting،
// Aspose.Words سوف يحل تضارب الأنماط عن طريق تحويل أنماط المستند المصدر.
// بنفس أسماء أنماط الوجهة في سمات الفقرة المباشرة.
ImportFormatOptions options = new ImportFormatOptions();
options.SmartStyleBehavior = true;

builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.SmartStyleBehavior.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
