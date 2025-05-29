---
title: StructuredDocumentTag.IsTemporary
linktitle: IsTemporary
articleTitle: IsTemporary
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تُحدد خاصية StructuredDocumentTag IsTemporary ما إذا كان سيتم إزالة SDT من WordProcessingML عند تغيير المحتوى. حسّن مستنداتك اليوم!
type: docs
weight: 160
url: /ar/net/aspose.words.markup/structureddocumenttag/istemporary/
---
## StructuredDocumentTag.IsTemporary property

يحدد ما إذا كان هذا**SDT** يجب إزالته من مستند WordProcessingML عند تعديل محتوياته .

```csharp
public bool IsTemporary { get; set; }
```

## أمثلة

يوضح كيفية إنشاء عناصر التحكم للاستخدام مرة واحدة.

```csharp
Document doc = new Document();

// إدراج علامة مستند منظم للنص العادي،
// والذي سيعمل كنموذج نص عادي يمكن للمستخدم إدخال النص فيه.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// اضبط خاصية "IsTemporary" على "true" لجعل علامة المستند المنظم تختفي و
//استيعاب محتوياته في المستند بعد أن يقوم المستخدم بتحريره مرة واحدة في Microsoft Word.
// اضبط خاصية "IsTemporary" على "false" للسماح للمستخدم بتحرير المحتويات
// من علامة المستند المنظم أي عدد من المرات.
tag.IsTemporary = isTemporary;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Please enter text: ");
builder.InsertNode(tag);

// قم بإدراج علامة مستند منظمة أخرى في شكل مربع اختيار وقم بتعيين حالتها الافتراضية إلى "محدد".
tag = new StructuredDocumentTag(doc, SdtType.Checkbox, MarkupLevel.Inline);
tag.Checked = true;

// اضبط الخاصية "IsTemporary" على "true" لجعل مربع الاختيار رمزًا
// بمجرد أن ينقر المستخدم عليه في Microsoft Word.
// قم بضبط الخاصية "IsTemporary" على "false" للسماح للمستخدم بالنقر فوق مربع الاختيار أي عدد من المرات.
tag.IsTemporary = isTemporary;

builder.Write("\nPlease click the check box: ");
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.IsTemporary.docx");
```

### أنظر أيضا

* class [StructuredDocumentTag](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
