---
title: PdfSaveOptions.CreateNoteHyperlinks
linktitle: CreateNoteHyperlinks
articleTitle: CreateNoteHyperlinks
second_title: Aspose.Words لـ .NET
description: حسّن ملفات PDF الخاصة بك باستخدام ميزة CreateNoteHyperlinks من PdfSaveOptions. حوّل الحواشي السفلية والختامية إلى روابط قابلة للنقر لسهولة التصفح. افتراضيًا، خطأ.
type: docs
weight: 60
url: /ar/net/aspose.words.saving/pdfsaveoptions/createnotehyperlinks/
---
## PdfSaveOptions.CreateNoteHyperlinks property

يحدد ما إذا كان سيتم تحويل مراجع الحواشي السفلية/الحواشي النهائية في القصة النصية الرئيسية إلى ارتباطات تشعبية نشطة. عند النقر فوق الارتباط التشعبي، سيقودك إلى الحاشية السفلية/الحواشي النهائية المقابلة. الإعداد الافتراضي هو`خطأ شنيع` .

```csharp
public bool CreateNoteHyperlinks { get; set; }
```

## أمثلة

يوضح كيفية جعل الحواشي السفلية والختامية تعمل كروابط تشعبية.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// اضبط خاصية "CreateNoteHyperlinks" على "true" لتحويل جميع رموز الحواشي السفلية/الختامية
// في النص تعمل كروابط، وعند النقر عليها تأخذنا إلى الحواشي السفلية/الختامية الخاصة بها.
// اضبط خاصية "CreateNoteHyperlinks" على "false" حتى لا ترتبط رموز الحاشية السفلية/النهاية بأي شيء.
options.CreateNoteHyperlinks = createNoteHyperlinks;

doc.Save(ArtifactsDir + "PdfSaveOptions.NoteHyperlinks.pdf", options);
```

### أنظر أيضا

* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
