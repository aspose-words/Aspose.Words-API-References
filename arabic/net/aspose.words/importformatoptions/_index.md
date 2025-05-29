---
title: ImportFormatOptions Class
linktitle: ImportFormatOptions
articleTitle: ImportFormatOptions
second_title: Aspose.Words لـ .NET
description: اكتشف خيارات Aspose.Words.ImportFormat لتنسيق مستندات قابل للتخصيص. حسّن مخرجاتك بإعدادات استيراد مخصصة لتحقيق أفضل النتائج.
type: docs
weight: 3690
url: /ar/net/aspose.words/importformatoptions/
---
## ImportFormatOptions class

يسمح بتحديد خيارات الاستيراد المختلفة لتنسيق الإخراج.

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
| [AdjustSentenceAndWordSpacing](../../aspose.words/importformatoptions/adjustsentenceandwordspacing/) { get; set; } | يحصل على قيمة منطقية أو يعينها لتحديد ما إذا كان سيتم تعديل المسافة بين الجمل والكلمات تلقائيًا. القيمة الافتراضية هي`خطأ شنيع` . |
| [ForceCopyStyles](../../aspose.words/importformatoptions/forcecopystyles/) { get; set; } | يحصل على قيمة منطقية أو يعينها للإشارة إلى نسخ الأنماط المتضاربة فيKeepSourceFormatting mode. القيمة الافتراضية هي`خطأ شنيع` . |
| [IgnoreHeaderFooter](../../aspose.words/importformatoptions/ignoreheaderfooter/) { get; set; } | يحصل على قيمة منطقية تحدد تنسيق المصدر لمحتوى الرؤوس/التذييلات الذي تم تجاهله إذاKeepSourceFormatting يتم استخدام الوضع. القيمة الافتراضية هي`حقيقي` . |
| [IgnoreTextBoxes](../../aspose.words/importformatoptions/ignoretextboxes/) { get; set; } | يحصل على قيمة منطقية تحدد تنسيق المصدر لمحتوى مربعات النص أو يعينها. يتم تجاهل إذاKeepSourceFormatting يتم استخدام الوضع. القيمة الافتراضية هي`حقيقي` . |
| [KeepSourceNumbering](../../aspose.words/importformatoptions/keepsourcenumbering/) { get; set; } | يحصل على قيمة منطقية أو يعينها لتحديد كيفية استيراد الترقيم عندما يتعارض في المستندات المصدر و الوجهة. القيمة الافتراضية هي`خطأ شنيع` . |
| [MergePastedLists](../../aspose.words/importformatoptions/mergepastedlists/) { get; set; } | يحصل على قيمة منطقية تحدد ما إذا كانت القوائم الملصقة سيتم دمجها مع القوائم المحيطة أم لا. القيمة الافتراضية هي`خطأ شنيع` . |
| [SmartStyleBehavior](../../aspose.words/importformatoptions/smartstylebehavior/) { get; set; } | يحصل على قيمة منطقية أو يعينها لتحديد كيفية استيراد الأنماط عندما يكون لها أسماء متساوية في المستندات المصدر والوجهة. القيمة الافتراضية هي`خطأ شنيع` . |

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

// استنساخ المستند وتحرير نمط "MyStyle" الخاص بالاستنساخ، بحيث يكون لونه مختلفًا عن اللون الأصلي.
// إذا قمنا بإدراج النسخة المستنسخة في المستند الأصلي، فإن النمطين اللذين يحملان نفس الاسم سوف يتسببان في حدوث تعارض.
Document srcDoc = dstDoc.Clone();
srcDoc.Styles["MyStyle"].Font.Color = Color.Red;

// عندما نقوم بتمكين SmartStyleBehavior واستخدام وضع تنسيق الاستيراد KeepSourceFormatting،
// سيقوم Aspose.Words بحل تضارب الأنماط عن طريق تحويل أنماط المستند المصدر.
// بنفس أسماء أنماط الوجهة في سمات الفقرة المباشرة.
ImportFormatOptions options = new ImportFormatOptions();
options.SmartStyleBehavior = true;

builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.SmartStyleBehavior.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
