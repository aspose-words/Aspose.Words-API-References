---
title: ImportFormatOptions.SmartStyleBehavior
linktitle: SmartStyleBehavior
articleTitle: SmartStyleBehavior
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تُحسّن خاصية ImportFormatOptions SmartStyleBehavior استيراد الأنماط ذات الأسماء المتشابهة في المستندات. خصّص عملية الاستيراد بسهولة!
type: docs
weight: 80
url: /ar/net/aspose.words/importformatoptions/smartstylebehavior/
---
## ImportFormatOptions.SmartStyleBehavior property

يحصل على قيمة منطقية أو يعينها لتحديد كيفية استيراد الأنماط عندما يكون لها أسماء متساوية في المستندات المصدر والوجهة. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool SmartStyleBehavior { get; set; }
```

## ملاحظات

عندما يكون هذا الخيار**مُمَكَّن** سيتم توسيع نمط المصدر إلى سمات مباشرة داخل مستند الوجهة a ، إذاKeepSourceFormatting يتم استخدام وضع الاستيراد.

عندما يكون هذا الخيار**عاجز**سيتم توسيع نمط المصدر فقط إذا كان مرقمًا. لن يتم تجاوز سمات الوجهة الموجودة، بما في ذلك القوائم.

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

* class [ImportFormatOptions](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
