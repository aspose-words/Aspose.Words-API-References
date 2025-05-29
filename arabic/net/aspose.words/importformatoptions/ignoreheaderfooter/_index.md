---
title: ImportFormatOptions.IgnoreHeaderFooter
linktitle: IgnoreHeaderFooter
articleTitle: IgnoreHeaderFooter
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ImportFormatOptions IgnoreHeaderFooter، وتحكم بتنسيق الرأس/التذييل في وضع KeepSourceFormatting. بسّط استيراد مستنداتك اليوم!
type: docs
weight: 40
url: /ar/net/aspose.words/importformatoptions/ignoreheaderfooter/
---
## ImportFormatOptions.IgnoreHeaderFooter property

يحصل على قيمة منطقية تحدد تنسيق المصدر لمحتوى الرؤوس/التذييلات الذي تم تجاهله إذاKeepSourceFormatting يتم استخدام الوضع. القيمة الافتراضية هي`حقيقي` .

```csharp
public bool IgnoreHeaderFooter { get; set; }
```

## أمثلة

يوضح كيفية تحديد تجاهل تنسيق المصدر أو عدم تنسيقه لمحتوى الرؤوس/التذييلات.

```csharp
Document dstDoc = new Document(MyDir + "Document.docx");
Document srcDoc = new Document(MyDir + "Header and footer types.docx");

// إذا كان 'IgnoreHeaderFooter' خاطئًا، فسيتم تغيير التنسيق الأصلي لمحتوى الرأس/التذييل
// من "أنواع الرأس والتذييل.docx" سيتم استخدامها.
// إذا كان 'IgnoreHeaderFooter' صحيحًا، فسيتم تغيير تنسيق محتوى الرأس/التذييل
// سيتم استخدام "Document.docx".
ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.IgnoreHeaderFooter = false;

dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, importFormatOptions);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.DoNotIgnoreHeaderFooter.docx");
```

### أنظر أيضا

* class [ImportFormatOptions](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
