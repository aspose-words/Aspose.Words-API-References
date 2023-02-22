---
title: ImportFormatOptions.IgnoreHeaderFooter
second_title: Aspose.Words لمراجع .NET API
description: ImportFormatOptions ملكية. الحصول على أو تعيين قيمة منطقية تحدد تنسيق المصدر لمحتوى الرؤوس / التذييلات الذي تم تجاهله_ إذاKeepSourceFormatting الوضع المستخدم . القيمة الافتراضية هيحقيقي .
type: docs
weight: 30
url: /ar/net/aspose.words/importformatoptions/ignoreheaderfooter/
---
## ImportFormatOptions.IgnoreHeaderFooter property

الحصول على أو تعيين قيمة منطقية تحدد تنسيق المصدر لمحتوى الرؤوس / التذييلات الذي تم تجاهله_ إذاKeepSourceFormatting الوضع المستخدم . القيمة الافتراضية هي`حقيقي` .

```csharp
public bool IgnoreHeaderFooter { get; set; }
```

### أمثلة

يوضح كيفية تحديد تجاهل أو عدم تنسيق المصدر لمحتوى الرؤوس / التذييلات.

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
* مساحة الاسم [Aspose.Words](../../importformatoptions/)
* المجسم [Aspose.Words](../../../)


