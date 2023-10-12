---
title: PdfSaveOptions.CreateNoteHyperlinks
second_title: Aspose.Words لمراجع .NET API
description: PdfSaveOptions ملكية. يحدد ما إذا كان سيتم تحويل مراجع الحواشي السفلية/التعليقات الختامية في القصة النصية الرئيسية إلى ارتباطات تشعبية نشطة. عند النقر فوق الارتباط التشعبي سيؤدي إلى الحاشية السفلية/التعليقات الختامية المقابلة. الافتراضي هوخطأ شنيع .
type: docs
weight: 50
url: /ar/net/aspose.words.saving/pdfsaveoptions/createnotehyperlinks/
---
## PdfSaveOptions.CreateNoteHyperlinks property

يحدد ما إذا كان سيتم تحويل مراجع الحواشي السفلية/التعليقات الختامية في القصة النصية الرئيسية إلى ارتباطات تشعبية نشطة. عند النقر فوق الارتباط التشعبي سيؤدي إلى الحاشية السفلية/التعليقات الختامية المقابلة. الافتراضي هو`خطأ شنيع` .

```csharp
public bool CreateNoteHyperlinks { get; set; }
```

### أمثلة

يوضح كيفية جعل الحواشي السفلية والتعليقات الختامية تعمل كارتباطات تشعبية.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// قم بتعيين خاصية "CreateNoteHyperlinks" على "true" لتحويل كافة رموز الحواشي السفلية/التعليقات الختامية
// في النص بمثابة روابط تنقلنا، عند النقر عليها، إلى الحواشي السفلية/التعليقات الختامية الخاصة بكل منها.
// قم بتعيين خاصية "CreateNoteHyperlinks" على "خطأ" حتى لا ترتبط رموز الحواشي السفلية/التعليقات الختامية بأي شيء.
options.CreateNoteHyperlinks = createNoteHyperlinks;

doc.Save(ArtifactsDir + "PdfSaveOptions.NoteHyperlinks.pdf", options);
```

### أنظر أيضا

* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../pdfsaveoptions/)
* المجسم [Aspose.Words](../../../)


