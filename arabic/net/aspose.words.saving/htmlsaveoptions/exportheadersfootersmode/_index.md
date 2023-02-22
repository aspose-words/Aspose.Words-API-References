---
title: HtmlSaveOptions.ExportHeadersFootersMode
second_title: Aspose.Words لمراجع .NET API
description: HtmlSaveOptions ملكية. يحدد كيفية إخراج الرؤوس والتذييلات إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هيPerSection لـ HTML / MHTML وNone لـ EPUB.
type: docs
weight: 170
url: /ar/net/aspose.words.saving/htmlsaveoptions/exportheadersfootersmode/
---
## HtmlSaveOptions.ExportHeadersFootersMode property

يحدد كيفية إخراج الرؤوس والتذييلات إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هيPerSection لـ HTML / MHTML وNone لـ EPUB.

```csharp
public ExportHeadersFootersMode ExportHeadersFootersMode { get; set; }
```

### ملاحظات

من الصعب إخراج الرؤوس والتذييلات بشكل مفيد إلى HTML لأن HTML غير مرقم.

عندما تكون هذه الخاصيةPerSection، تصدر Aspose.Words الرؤوس والتذييلات الأولية فقط في بداية ونهاية كل قسم.

عندما يكونFirstSectionHeaderLastSectionFooter يتم تصدير الرأس الأساسي الأول فقط والتذييل الأساسي الأخير (بما في ذلك المرتبط بالسابق).

يمكنك تعطيل تصدير الرؤوس والتذييلات تمامًا عن طريق تعيين هذه property إلىNone.

### أمثلة

يوضح كيفية حذف الرؤوس / التذييلات عند حفظ مستند بتنسيق HTML.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// يحتوي هذا المستند على رؤوس وتذييلات. يمكننا الوصول إليهم عبر مجموعة "HeadersFooters".
Assert.AreEqual("First header", doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderFirst].GetText().Trim());

// لا تقسّم التنسيقات مثل .html المستند إلى صفحات ، لذا لن تعمل الرؤوس / التذييلات بالطريقة نفسها
// سيفعلون ذلك عندما نفتح المستند بتنسيق docx. باستخدام Microsoft Word.
// إذا قمنا بتحويل مستند يحتوي على رؤوس / تذييلات إلى html ، فسيؤدي التحويل إلى استيعاب الرؤوس / التذييلات في نص أساسي.
// يمكننا استخدام كائن SaveOptions لحذف الرؤوس / التذييلات أثناء التحويل إلى html.
HtmlSaveOptions saveOptions =
    new HtmlSaveOptions(SaveFormat.Html) { ExportHeadersFootersMode = ExportHeadersFootersMode.None };

doc.Save(ArtifactsDir + "HeaderFooter.ExportMode.html", saveOptions);

// افتح المستند المحفوظ وتحقق من أنه لا يحتوي على نص الرأس
doc = new Document(ArtifactsDir + "HeaderFooter.ExportMode.html");

Assert.IsFalse(doc.Range.Text.Contains("First header"));
```

### أنظر أيضا

* enum [ExportHeadersFootersMode](../../exportheadersfootersmode/)
* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../htmlsaveoptions/)
* المجسم [Aspose.Words](../../../)


