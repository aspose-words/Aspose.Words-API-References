---
title: ImportFormatOptions.IgnoreHeaderFooter
linktitle: IgnoreHeaderFooter
articleTitle: IgnoreHeaderFooter
second_title: Aspose.Words لـ .NET
description: ImportFormatOptions IgnoreHeaderFooter ملكية. الحصول على أو تعيين قيمة منطقية تحدد تنسيق المصدر لمحتوى الرؤوس/التذييلات الذي تم تجاهله إذاKeepSourceFormatting يتم استخدام الوضع. القيمة الافتراضية هيحقيقي  في C#.
type: docs
weight: 40
url: /ar/net/aspose.words/importformatoptions/ignoreheaderfooter/
---
## ImportFormatOptions.IgnoreHeaderFooter property

الحصول على أو تعيين قيمة منطقية تحدد تنسيق المصدر لمحتوى الرؤوس/التذييلات الذي تم تجاهله إذاKeepSourceFormatting يتم استخدام الوضع. القيمة الافتراضية هي`حقيقي` .

```csharp
public bool IgnoreHeaderFooter { get; set; }
```

## أمثلة

يوضح كيفية تحديد تجاهل أو عدم تنسيق المصدر لمحتوى الرؤوس/التذييلات.

```csharp
Document dstDoc = new Document(MyDir + "Document.docx");
Document srcDoc = new Document(MyDir + "Header and footer types.docx");

ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.IgnoreHeaderFooter = false;

dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, importFormatOptions);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.DoNotIgnoreHeaderFooter.docx");
```

### أنظر أيضا

* class [ImportFormatOptions](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
