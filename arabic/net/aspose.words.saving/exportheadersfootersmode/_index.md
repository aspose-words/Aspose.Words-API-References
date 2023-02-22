---
title: Enum ExportHeadersFootersMode
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Saving.ExportHeadersFootersMode تعداد. يحدد كيفية تصدير الرؤوس والتذييلات إلى HTML أو MHTML أو EPUB.
type: docs
weight: 4740
url: /ar/net/aspose.words.saving/exportheadersfootersmode/
---
## ExportHeadersFootersMode enumeration

يحدد كيفية تصدير الرؤوس والتذييلات إلى HTML أو MHTML أو EPUB.

```csharp
public enum ExportHeadersFootersMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | لا يتم تصدير الرؤوس والتذييلات . |
| PerSection | `1` | يتم تصدير الرؤوس والتذييلات الأساسية في بداية ونهاية كل قسم. |
| FirstSectionHeaderLastSectionFooter | `2` | يتم تصدير الرأس الأساسي للقسم الأول في بداية المستند والتذييل الأساسي في النهاية. |
| FirstPageHeaderFooterPerSection | `3` | يتم تصدير رأس الصفحة الأولى وتذييلها في بداية ونهاية كل قسم. |

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

* property [ExportHeadersFootersMode](../htmlsaveoptions/exportheadersfootersmode/)
* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)


