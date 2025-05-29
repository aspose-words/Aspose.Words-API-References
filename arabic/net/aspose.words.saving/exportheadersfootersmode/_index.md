---
title: ExportHeadersFootersMode Enum
linktitle: ExportHeadersFootersMode
articleTitle: ExportHeadersFootersMode
second_title: Aspose.Words لـ .NET
description: اكتشف وضع تصدير Aspose.Words للرؤوس والتذييلات بسلاسة بصيغ HTML أو MHTML أو EPUB. حسّن تحويل مستنداتك اليوم!
type: docs
weight: 5750
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
| None | `0` | لا يتم تصدير الرؤوس والتذييلات. |
| PerSection | `1` | يتم تصدير الرؤوس والتذييلات الأساسية في بداية ونهاية كل قسم. |
| FirstSectionHeaderLastSectionFooter | `2` | يتم تصدير الرأس الرئيسي للقسم الأول في بداية المستند والتذييل الرئيسي في النهاية. |
| FirstPageHeaderFooterPerSection | `3` | يتم تصدير رأس وتذييل الصفحة الأولى في بداية ونهاية كل قسم. |

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

* property [ExportHeadersFootersMode](../htmlsaveoptions/exportheadersfootersmode/)
* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
