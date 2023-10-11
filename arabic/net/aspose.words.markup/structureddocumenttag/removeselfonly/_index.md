---
title: StructuredDocumentTag.RemoveSelfOnly
second_title: Aspose.Words لمراجع .NET API
description: StructuredDocumentTag طريقة. إزالة عقدة SDT نفسها فقط مع الاحتفاظ بمحتواها داخل شجرة المستندات.
type: docs
weight: 370
url: /ar/net/aspose.words.markup/structureddocumenttag/removeselfonly/
---
## StructuredDocumentTag.RemoveSelfOnly method

إزالة عقدة SDT نفسها فقط، مع الاحتفاظ بمحتواها داخل شجرة المستندات.

```csharp
public void RemoveSelfOnly()
```

### أمثلة

يوضح كيفية إنشاء علامة مستند منظمة في مربع نص عادي وتعديل مظهرها.

```csharp
Document doc = new Document();

// قم بإنشاء علامة مستند منظمة تحتوي على نص عادي.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// قم بتعيين عنوان ولون الإطار الذي يظهر عند تمرير الماوس فوق علامة المستند المنظم في Microsoft Word.
tag.Title = "My plain text";
tag.Color = Color.Magenta;

// قم بتعيين علامة لعلامة المستند المنظمة هذه، والتي يمكن الحصول عليها
// كعنصر XML يُسمى "tag"، مع السلسلة الموجودة أدناه في السمة "@val" الخاصة به.
tag.Tag = "MyPlainTextSDT";

// كل علامة مستند منظمة لها معرف فريد عشوائي.
Assert.That(tag.Id, Is.Positive);

// قم بتعيين الخط للنص داخل علامة المستند المنظم.
tag.ContentsFont.Name = "Arial";

// قم بتعيين الخط للنص الموجود في نهاية علامة المستند المنظمة.
// أي نص نكتبه في نص المستند بعد الخروج من العلامة باستخدام مفاتيح الأسهم سيستخدم هذا الخط.
tag.EndCharacterFont.Name = "Arial Black";

// بشكل افتراضي، هذا خطأ والضغط على زر الإدخال أثناء وجودك داخل علامة مستند منظمة لا يؤدي إلى أي شيء.
// عند التعيين على "صحيح"، يمكن أن تحتوي علامة المستند المنظمة لدينا على عدة أسطر.

// اضبط الخاصية "متعدد الأسطر" على "خطأ" للسماح بالمحتويات فقط
// من علامة المستند المنظمة هذه لتمتد على سطر واحد.
// اضبط الخاصية "متعدد الأسطر" على "صحيح" للسماح للعلامة باحتواء أسطر متعددة من المحتوى.
tag.Multiline = true;

// قم بتعيين خاصية "المظهر" على "SdtAppearance.Tags" لإظهار العلامات حول المحتوى.
 // افتراضيًا، تظهر علامة المستند المنظمة كـ BoundingBox.
tag.Appearance = SdtAppearance.Tags;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(tag);

// أدخل نسخة من علامة المستند المنظمة في فقرة جديدة.
StructuredDocumentTag tagClone = (StructuredDocumentTag)tag.Clone(true);
builder.InsertParagraph();
builder.InsertNode(tagClone);

// استخدم طريقة "RemoveSelfOnly" لإزالة علامة مستند منظم، مع الاحتفاظ بمحتوياتها في المستند.
tagClone.RemoveSelfOnly();

doc.Save(ArtifactsDir + "StructuredDocumentTag.PlainText.docx");
```

### أنظر أيضا

* class [StructuredDocumentTag](../)
* مساحة الاسم [Aspose.Words.Markup](../../structureddocumenttag/)
* المجسم [Aspose.Words](../../../)


