---
title: Enum DocumentSplitCriteria
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Saving.DocumentSplitCriteria تعداد. يحدد كيفية تقسيم المستند إلى أجزاء عند الحفظ فيهHtmlEpub أوAzw3 التنسيق.
type: docs
weight: 4960
url: /ar/net/aspose.words.saving/documentsplitcriteria/
---
## DocumentSplitCriteria enumeration

يحدد كيفية تقسيم المستند إلى أجزاء عند الحفظ فيهHtmlEpub أوAzw3 التنسيق.

```csharp
[Flags]
public enum DocumentSplitCriteria
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | لم يتم تقسيم المستند. |
| PageBreak | `1` | يتم تقسيم المستند إلى أجزاء عند فواصل الصفحات الصريحة. يمكن تحديد فاصل الصفحات بواسطة[`PageBreak`](../../aspose.words/controlchar/pagebreak/) الحرف، فاصل مقطعي يحدد بداية قسم جديد في صفحة جديدة، أو فقرة لها[`PageBreakBefore`](../../aspose.words/paragraphformat/pagebreakbefore/) خاصية تعيين ل`حقيقي` . |
| ColumnBreak | `2` | يتم تقسيم المستند إلى أجزاء عند فواصل الأعمدة. يمكن تحديد فاصل الأعمدة بواسطة[`ColumnBreak`](../../aspose.words/controlchar/columnbreak/) الحرف أو فاصل مقطعي يحدد بداية قسم جديد في عمود جديد. |
| SectionBreak | `4` | يتم تقسيم المستند إلى أجزاء عند فاصل مقطعي من أي نوع. |
| HeadingParagraph | `8` | يتم تقسيم المستند إلى أجزاء في فقرة منسقة باستخدام نمط العنوان **عنوان 1** , **العنوان 2** إلخ. استخدمه مع[`DocumentSplitHeadingLevel`](../htmlsaveoptions/documentsplitheadinglevel/) لتحديد مستويات العناوين (من 1 إلى المستوى المحدد) التي سيتم التقسيم عندها. |

### ملاحظات

`DocumentSplitCriteria`هي مجموعة من الأعلام التي يمكن دمجها. على سبيل المثال، يمكنك تقسيم document عند فواصل الصفحات وفقرات العناوين في نفس عملية التصدير.

يمكن أن تتداخل المعايير المختلفة جزئيًا. على سبيل المثال، **عنوان 1** يتم إعطاء النمط بشكل متكرر [`PageBreakBefore`](../../aspose.words/paragraphformat/pagebreakbefore/) الملكية لذلك تندرج تحت معيارين:PageBreak و HeadingParagraph. قد تؤدي بعض فواصل الأقسام إلى حدوث فواصل للصفحات وما إلى ذلك. في الحالات النموذجية، يكون تحديد علامة واحدة فقط هو الخيار الأكثر عملية.

### أمثلة

يوضح كيفية استخدام ترميز معين عند حفظ مستند إلى .epub.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// استخدم كائن SaveOptions لتحديد ترميز المستند الذي سنقوم بحفظه.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// بشكل افتراضي، سيحتوي مستند الإخراج .epub على جميع محتوياته في جزء HTML واحد.
// يسمح لنا معيار التقسيم بتقسيم المستند إلى عدة أجزاء بتنسيق HTML.
// سنضع المعايير لتقسيم الوثيقة إلى فقرات رأسية.
// هذا مفيد للقراء الذين لا يستطيعون قراءة ملفات HTML ذات حجم أكبر من حجم معين.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// حدد أننا نريد تصدير خصائص المستند.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)


