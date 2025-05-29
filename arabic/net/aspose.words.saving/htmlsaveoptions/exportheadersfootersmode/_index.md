---
title: HtmlSaveOptions.ExportHeadersFootersMode
linktitle: ExportHeadersFootersMode
articleTitle: ExportHeadersFootersMode
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تُحسّن خاصية HtmlSaveOptions ExportHeadersFootersMode مخرجات الرأس والتذييل لتنسيقات HTML وMHTML وEPUB. حسّن عرض مستندك إلى أقصى حد!
type: docs
weight: 160
url: /ar/net/aspose.words.saving/htmlsaveoptions/exportheadersfootersmode/
---
## HtmlSaveOptions.ExportHeadersFootersMode property

يحدد كيفية إخراج الرؤوس والتذييلات إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هيPerSection لـ HTML/MHTML وNone لـ EPUB.

```csharp
public ExportHeadersFootersMode ExportHeadersFootersMode { get; set; }
```

## ملاحظات

من الصعب إخراج الرؤوس والتذييلات بشكل مفيد إلى HTML لأن HTML ليس مقسمًا إلى صفحات.

عندما تكون هذه الخاصيةPerSectionيقوم Aspose.Words بتصدير الرؤوس والتذييلات الأساسية فقط في بداية ونهاية كل قسم.

عندما يكونFirstSectionHeaderLastSectionFooter يتم تصدير فقط الرأس الأساسي الأول والتذييل الأساسي الأخير (بما في ذلك المرتبط بالسابق).

يمكنك تعطيل تصدير الرؤوس والتذييلات بالكامل عن طريق تعيين هذه الخاصية إلىNone.

## أمثلة

يوضح كيفية حذف الرؤوس/التذييلات عند حفظ مستند بتنسيق HTML.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// تحتوي هذه الوثيقة على رؤوس وتذييلات. يُمكن الوصول إليها عبر مجموعة "الرؤوس والتذييلات".
Assert.AreEqual("First header", doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderFirst].GetText().Trim());

// لا تقوم التنسيقات مثل .html بتقسيم المستند إلى صفحات، لذا لن تعمل الرؤوس/التذييلات بنفس الطريقة
//سيحدث ذلك عندما نفتح المستند بصيغة .docx باستخدام Microsoft Word.
// إذا قمنا بتحويل مستند يحتوي على رؤوس/تذييلات إلى HTML، فسوف يقوم التحويل بدمج الرؤوس/التذييلات في نص أساسي.
// يمكننا استخدام كائن SaveOptions لحذف الرؤوس/التذييلات أثناء التحويل إلى html.
HtmlSaveOptions saveOptions =
    new HtmlSaveOptions(SaveFormat.Html) { ExportHeadersFootersMode = ExportHeadersFootersMode.None };

doc.Save(ArtifactsDir + "HeaderFooter.ExportMode.html", saveOptions);

// افتح المستند المحفوظ لدينا وتأكد من أنه لا يحتوي على نص الرأس
doc = new Document(ArtifactsDir + "HeaderFooter.ExportMode.html");

Assert.IsFalse(doc.Range.Text.Contains("First header"));
```

### أنظر أيضا

* enum [ExportHeadersFootersMode](../../exportheadersfootersmode/)
* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
