---
title: HtmlFixedSaveOptions.OptimizeOutput
second_title: Aspose.Words لمراجع .NET API
description: HtmlFixedSaveOptions ملكية. تشير العلامة إلى ما إذا كان مطلوبًا تحسين الإخراج. إذا تم تعيين هذه العلامة للوحات القماشية المتداخلة الزائدة وتمت إزالة اللوحات الفارغة يتم أيضًا ربط الحروف الرسومية المجاورة بنفس التنسيق. ملاحظة قد تتأثر دقة عرض المحتوى إذا تم تعيين هذه الخاصية علىحقيقي . الافتراضي هوحقيقي .
type: docs
weight: 100
url: /ar/net/aspose.words.saving/htmlfixedsaveoptions/optimizeoutput/
---
## HtmlFixedSaveOptions.OptimizeOutput property

تشير العلامة إلى ما إذا كان مطلوبًا تحسين الإخراج. إذا تم تعيين هذه العلامة للوحات القماشية المتداخلة الزائدة وتمت إزالة اللوحات الفارغة، يتم أيضًا ربط الحروف الرسومية المجاورة بنفس التنسيق. ملاحظة: قد تتأثر دقة عرض المحتوى إذا تم تعيين هذه الخاصية على`حقيقي` . الافتراضي هو`حقيقي` .

```csharp
public override bool OptimizeOutput { get; set; }
```

### أمثلة

يوضح كيفية تبسيط مستند عند حفظه بتنسيق HTML عن طريق إزالة العديد من الكائنات الزائدة عن الحاجة.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions { OptimizeOutput = optimizeOutput };

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html", saveOptions);

// يبلغ حجم النسخة المحسنة من المستند ما يقرب من ثلث حجم المستند غير المحسن.
Assert.AreEqual(optimizeOutput ? 62521 : 191770,
    new FileInfo(ArtifactsDir + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html").Length, 200);
```

### أنظر أيضا

* class [HtmlFixedSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* المجسم [Aspose.Words](../../../)


