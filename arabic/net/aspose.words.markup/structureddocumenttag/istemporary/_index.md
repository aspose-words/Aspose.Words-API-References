---
title: StructuredDocumentTag.IsTemporary
second_title: Aspose.Words لمراجع .NET API
description: StructuredDocumentTag ملكية. يحدد ما إذا كان هذا المعاملة الخاصة والتفضيلية ستتم إزالته من مستند WordProcessingML عند تعديل محتوياته .
type: docs
weight: 160
url: /ar/net/aspose.words.markup/structureddocumenttag/istemporary/
---
## StructuredDocumentTag.IsTemporary property

يحدد ما إذا كان هذا **المعاملة الخاصة والتفضيلية** ستتم إزالته من مستند WordProcessingML عند تعديل محتوياته .

```csharp
public bool IsTemporary { get; set; }
```

### أمثلة

يوضح كيفية إنشاء عناصر تحكم للاستخدام الفردي.

```csharp
Document doc = new Document();

// أدخل علامة مستند منظم بنص عادي،
// والذي سيكون بمثابة نموذج نص عادي يمكن للمستخدم إدخال النص فيه.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// اضبط الخاصية "IsTemporary" على "true" حتى تختفي علامة المستند المنظمة و
// استيعاب محتوياته في المستند بعد أن يقوم المستخدم بتحريره مرة واحدة في Microsoft Word.
// اضبط الخاصية "IsTemporary" على "خطأ" للسماح للمستخدم بتحرير المحتويات
// لعلامة الوثيقة المنظمة أي عدد من المرات.
tag.IsTemporary = isTemporary;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Please enter text: ");
builder.InsertNode(tag);

// أدخل علامة مستند منظمة أخرى في شكل مربع اختيار وقم بتعيين حالتها الافتراضية على "محدد".
tag = new StructuredDocumentTag(doc, SdtType.Checkbox, MarkupLevel.Inline);
tag.Checked = true;

// اضبط الخاصية "IsTemporary" على "صحيح" لجعل خانة الاختيار رمزًا
// بمجرد أن ينقر المستخدم عليه في Microsoft Word.
// اضبط الخاصية "IsTemporary" على "خطأ" للسماح للمستخدم بالنقر فوق خانة الاختيار لأي عدد من المرات.
tag.IsTemporary = isTemporary;

builder.Write("\nPlease click the check box: ");
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.IsTemporary.docx");
```

### أنظر أيضا

* class [StructuredDocumentTag](../)
* مساحة الاسم [Aspose.Words.Markup](../../structureddocumenttag/)
* المجسم [Aspose.Words](../../../)


