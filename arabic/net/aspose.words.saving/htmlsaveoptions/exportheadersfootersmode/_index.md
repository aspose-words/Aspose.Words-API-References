---
title: HtmlSaveOptions.ExportHeadersFootersMode
linktitle: ExportHeadersFootersMode
articleTitle: ExportHeadersFootersMode
second_title: Aspose.Words لـ .NET
description: HtmlSaveOptions ExportHeadersFootersMode ملكية. يحدد كيفية إخراج الرؤوس والتذييلات إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هيPerSection لـ HTML/MHTML وNone لـ EPUB في C#.
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

من الصعب إخراج الرؤوس والتذييلات إلى HTML بشكل مفيد لأن HTML غير مرقّم.

عندما تكون هذه الخاصيةPerSectionيقوم Aspose.Words بتصدير فقط الرؤوس والتذييلات الأساسية في بداية ونهاية كل قسم.

عندما يكونFirstSectionHeaderLastSectionFooter يتم تصدير فقط الرأس الأساسي الأول والتذييل الأساسي الأخير (بما في ذلك المرتبط بالسابق).

يمكنك تعطيل تصدير الرؤوس والتذييلات تمامًا عن طريق تعيين هذه الخاصية property علىNone.

## أمثلة

يوضح كيفية حذف الرؤوس/التذييلات عند حفظ مستند إلى HTML.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// يحتوي هذا المستند على الرؤوس والتذييلات. يمكننا الوصول إليها عبر مجموعة "HeadersFooters".
Assert.AreEqual("First header", doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderFirst].GetText().Trim());

// تنسيقات مثل .html لا تقسم المستند إلى صفحات، لذلك لن تعمل الرؤوس والتذييلات بنفس الطريقة
// سيفعلون ذلك عندما نفتح المستند بتنسيق .docx باستخدام Microsoft Word.
// إذا قمنا بتحويل مستند يحتوي على رؤوس/تذييلات إلى html، فسيؤدي التحويل إلى دمج الرؤوس/التذييلات في نص أساسي.
// يمكننا استخدام كائن SaveOptions لحذف الرؤوس/التذييلات أثناء التحويل إلى html.
HtmlSaveOptions saveOptions =
    new HtmlSaveOptions(SaveFormat.Html) { ExportHeadersFootersMode = ExportHeadersFootersMode.None };

doc.Save(ArtifactsDir + "HeaderFooter.ExportMode.html", saveOptions);

// افتح مستندنا المحفوظ وتأكد من أنه لا يحتوي على نص الرأس
doc = new Document(ArtifactsDir + "HeaderFooter.ExportMode.html");

Assert.IsFalse(doc.Range.Text.Contains("First header"));
```

### أنظر أيضا

* enum [ExportHeadersFootersMode](../../exportheadersfootersmode/)
* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
