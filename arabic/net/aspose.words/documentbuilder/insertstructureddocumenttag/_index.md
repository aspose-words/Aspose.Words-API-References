---
title: DocumentBuilder.InsertStructuredDocumentTag
linktitle: InsertStructuredDocumentTag
articleTitle: InsertStructuredDocumentTag
second_title: Aspose.Words لـ .NET
description: حسّن مستنداتك بسهولة باستخدام طريقة InsertStructuredDocumentTag في DocumentBuilder. أضف بسهولة وسومًا منظمة للمستندات لتحسين التنظيم!
type: docs
weight: 480
url: /ar/net/aspose.words/documentbuilder/insertstructureddocumenttag/
---
## DocumentBuilder.InsertStructuredDocumentTag method

يُدرج[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) في المستند.

```csharp
public StructuredDocumentTag InsertStructuredDocumentTag(SdtType type)
```

### قيمة الإرجاع

ال[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) العقدة التي تم إدخالها للتو.

## أمثلة

يوضح كيفية إدراج علامة مستند منظمة ببساطة.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveTo(doc.FirstSection.Body.Paragraphs[3]);
// لاحظ أنه يُسمح فقط بأنواع StructuredDocumentTag التالية للإدراج:
// SdtType.PlainText، SdtType.RichText، SdtType.Checkbox، SdtType.DropDownList،
// SdtType.ComboBox، SdtType.Picture، SdtType.Date.
// سيتم اكتشاف مستوى ترميز StructuredDocumentTag المدرج تلقائيًا ويعتمد على الموضع الذي يتم إدراجه فيه.
// تمت إضافة StructuredDocumentTag الذي سيرث تنسيق الفقرة والخط من موضع المؤشر.
StructuredDocumentTag sdtPlain = builder.InsertStructuredDocumentTag(SdtType.PlainText);

doc.Save(ArtifactsDir + "StructuredDocumentTag.InsertStructuredDocumentTag.docx");
```

### أنظر أيضا

* class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* enum [SdtType](../../../aspose.words.markup/sdttype/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
