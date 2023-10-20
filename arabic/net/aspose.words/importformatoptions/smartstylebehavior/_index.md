---
title: ImportFormatOptions.SmartStyleBehavior
linktitle: SmartStyleBehavior
articleTitle: SmartStyleBehavior
second_title: Aspose.Words لـ .NET
description: ImportFormatOptions SmartStyleBehavior ملكية. الحصول على أو تعيين قيمة منطقية تحدد كيفية استيراد الأنماط عندما يكون لها أسماء متساوية في المستندات المصدر والوجهة. القيمة الافتراضية هيخطأ شنيع  في C#.
type: docs
weight: 80
url: /ar/net/aspose.words/importformatoptions/smartstylebehavior/
---
## ImportFormatOptions.SmartStyleBehavior property

الحصول على أو تعيين قيمة منطقية تحدد كيفية استيراد الأنماط عندما يكون لها أسماء متساوية في المستندات المصدر والوجهة. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool SmartStyleBehavior { get; set; }
```

## ملاحظات

عندما يكون هذا الخيار**ممكّن** ، سيتم توسيع النمط المصدر إلى سمات مباشرة داخل مستند الوجهة a ، إذاKeepSourceFormatting يتم استخدام وضع الاستيراد.

عندما يكون هذا الخيار**عاجز**، سيتم توسيع نمط المصدر فقط إذا كان مرقمًا. لن يتم تجاوز سمات الوجهة Existing ، بما في ذلك القوائم.

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

* class [ImportFormatOptions](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
