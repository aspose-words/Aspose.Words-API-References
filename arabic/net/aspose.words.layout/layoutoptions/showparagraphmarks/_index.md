---
title: LayoutOptions.ShowParagraphMarks
second_title: Aspose.Words لمراجع .NET API
description: LayoutOptions ملكية. الحصول على أو تعيين إشارة إلى ما إذا كان يتم تقديم علامات الفقرات. الإعداد الافتراضي هو False .
type: docs
weight: 80
url: /ar/net/aspose.words.layout/layoutoptions/showparagraphmarks/
---
## LayoutOptions.ShowParagraphMarks property

الحصول على أو تعيين إشارة إلى ما إذا كان يتم تقديم علامات الفقرات. الإعداد الافتراضي هو False .

```csharp
public bool ShowParagraphMarks { get; set; }
```

### أمثلة

يوضح كيفية إظهار علامات الفقرات في مستند الإخراج الذي تم تقديمه.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// أضف بعض الفقرات ، ثم قم بتمكين علامات الفقرات لإظهار نهايات الفقرات
// مع رمز بيلكرو (¶) عند تقديم المستند.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

### أنظر أيضا

* class [LayoutOptions](../)
* مساحة الاسم [Aspose.Words.Layout](../../layoutoptions/)
* المجسم [Aspose.Words](../../../)


