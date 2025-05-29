---
title: PdfPageLayout Enum
linktitle: PdfPageLayout
articleTitle: PdfPageLayout
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.Saving.PdfPageLayout enum لعرض مثالي لملفات PDF. خصّص تخطيطات الصفحات لتحسين قابلية القراءة في أي قارئ PDF.
type: docs
weight: 6290
url: /ar/net/aspose.words.saving/pdfpagelayout/
---
## PdfPageLayout enumeration

يحدد تخطيط الصفحة الذي سيتم استخدامه عند فتح المستند في قارئ PDF.

```csharp
public enum PdfPageLayout
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| SinglePage | `0` | عرض صفحة واحدة في كل مرة. |
| OneColumn | `1` | عرض الصفحات في عمود واحد. |
| TwoColumnLeft | `2` | عرض الصفحات في عمودين، مع وضع الصفحات ذات الأرقام الفردية على اليسار. |
| TwoColumnRight | `3` | عرض الصفحات في عمودين، مع وضع الصفحات ذات الأرقام الفردية على اليمين. |
| TwoPageLeft | `4` | عرض الصفحات صفحتين في كل مرة، مع وضع الصفحات ذات الأرقام الفردية على اليسار. |
| TwoPageRight | `5` | عرض الصفحات صفحتين في كل مرة، مع الصفحات ذات الأرقام الفردية على اليمين. |

## أمثلة

يوضح كيفية عرض الصفحات عند فتحها في قارئ PDF.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// عرض الصفحات صفحتين في كل مرة، مع وضع الصفحات ذات الأرقام الفردية على اليسار.
PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.PageLayout = PdfPageLayout.TwoPageLeft;

doc.Save(ArtifactsDir + "PdfSaveOptions.PageLayout.pdf", saveOptions);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
