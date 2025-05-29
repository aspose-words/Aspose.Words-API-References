---
title: DocumentSplitCriteria Enum
linktitle: DocumentSplitCriteria
articleTitle: DocumentSplitCriteria
second_title: Aspose.Words لـ .NET
description: اكتشف كيف يُحسّن Aspose.Words.Saving.DocumentSplitCriteria تقسيم المستندات للحصول على أفضل صيغ HTML وEpub وAzw3. بسّط عملية الحفظ!
type: docs
weight: 5710
url: /ar/net/aspose.words.saving/documentsplitcriteria/
---
## DocumentSplitCriteria enumeration

يحدد كيفية تقسيم المستند إلى أجزاء عند الحفظ فيHtml ، Epub أوAzw3 تنسيق.

```csharp
[Flags]
public enum DocumentSplitCriteria
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | لم يتم تقسيم المستند. |
| PageBreak | `1` | يتم تقسيم المستند إلى أجزاء عند فواصل الصفحات الصريحة. يمكن تحديد فاصل الصفحة بواسطة[`PageBreak`](../../aspose.words/controlchar/pagebreak/) حرف، فاصل قسم يحدد بداية قسم جديد على صفحة جديدة، أو فقرة لها[`PageBreakBefore`](../../aspose.words/paragraphformat/pagebreakbefore/) تم تعيين الخاصية إلى`حقيقي` . |
| ColumnBreak | `2` | يتم تقسيم المستند إلى أجزاء عند فواصل الأعمدة. يمكن تحديد فواصل الأعمدة بواسطة[`ColumnBreak`](../../aspose.words/controlchar/columnbreak/) حرف or فاصل قسم يحدد بداية قسم جديد في عمود جديد. |
| SectionBreak | `4` | يتم تقسيم المستند إلى أجزاء عند وجود أي نوع من أنواع فاصل الأقسام. |
| HeadingParagraph | `8` | يتم تقسيم المستند إلى أجزاء في فقرة منسقة باستخدام نمط العنوان**العنوان 1** ،**العنوان 2** إلخ. استخدم مع[`DocumentSplitHeadingLevel`](../htmlsaveoptions/documentsplitheadinglevel/) لتحديد مستويات العنوان (من 1 إلى المستوى المحدد) التي سيتم تقسيمها. |

## ملاحظات

`DocumentSplitCriteria`مجموعة من العلامات التي يمكن دمجها. على سبيل المثال، يمكنك تقسيم document عند فواصل الصفحات وعناوين الفقرات في عملية التصدير نفسها.

قد تتداخل المعايير المختلفة جزئيًا. على سبيل المثال،**العنوان 1** يتم إعطاء النمط بشكل متكرر [`PageBreakBefore`](../../aspose.words/paragraphformat/pagebreakbefore/) الممتلكات لذلك فهي تندرج تحت معيارين:PageBreak و HeadingParagraph. قد تتسبب بعض فواصل الأقسام في حدوث فواصل للصفحات وما إلى ذلك. في الحالات النموذجية، يعد تحديد علم واحد فقط هو الخيار الأكثر عملية.

## أمثلة

يوضح كيفية استخدام ترميز معين عند حفظ مستند بتنسيق .epub.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// استخدم كائن SaveOptions لتحديد الترميز للمستند الذي سنحفظه.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// بشكل افتراضي، سيكون مستند .epub الناتج يحتوي على كل محتوياته في جزء HTML واحد.
// يسمح لنا معيار التقسيم بتقسيم المستند إلى عدة أجزاء HTML.
// سوف نقوم بتحديد المعايير لتقسيم المستند إلى فقرات عنوانية.
// يعد هذا مفيدًا للقراء الذين لا يستطيعون قراءة ملفات HTML ذات حجم أكبر من حجم معين.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// حدد أننا نريد تصدير خصائص المستند.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
