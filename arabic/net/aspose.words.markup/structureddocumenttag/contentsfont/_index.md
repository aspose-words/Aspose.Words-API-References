---
title: StructuredDocumentTag.ContentsFont
linktitle: ContentsFont
articleTitle: ContentsFont
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية StructuredDocumentTag ContentsFont لتنسيق نصوص سلس في SDT. حسّن مستنداتك بخيارات خطوط قابلة للتخصيص!
type: docs
weight: 80
url: /ar/net/aspose.words.markup/structureddocumenttag/contentsfont/
---
## StructuredDocumentTag.ContentsFont property

تنسيق الخط الذي سيتم تطبيقه على النص المدخل في**SDT** .

```csharp
public Font ContentsFont { get; }
```

## أمثلة

يوضح كيفية إنشاء علامة مستند منظمة في مربع نص عادي وتعديل مظهرها.

```csharp
Document doc = new Document();

// قم بإنشاء علامة مستند منظمة تحتوي على نص عادي.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// تعيين عنوان ولون الإطار الذي يظهر عند تحريك مؤشر الماوس فوق علامة المستند المنظم في Microsoft Word.
tag.Title = "My plain text";
tag.Color = Color.Magenta;

// قم بتعيين علامة لهذه العلامة المستندة المنظمة، والتي يمكن الحصول عليها
// كعنصر XML يسمى "tag"، مع السلسلة أدناه في سمة "@val".
tag.Tag = "MyPlainTextSDT";

// كل علامة مستند منظمة لها معرف فريد عشوائي.
Assert.IsTrue(tag.Id > 0);

// تعيين الخط للنص داخل علامة المستند المنظم.
tag.ContentsFont.Name = "Arial";

// تعيين الخط للنص في نهاية علامة المستند المنظم.
// أي نص نكتبه في نص المستند بعد الخروج من العلامة باستخدام مفاتيح الأسهم سوف يستخدم هذا الخط.
tag.EndCharacterFont.Name = "Arial Black";

// بشكل افتراضي، هذا خطأ والضغط على مفتاح الإدخال أثناء وجودك داخل علامة مستند منظم لا يؤدي إلى أي شيء.
// عند ضبطه على true، يمكن أن يحتوي علامة المستند المنظم لدينا على أسطر متعددة.

// اضبط خاصية "متعدد الأسطر" على "خطأ" للسماح فقط بالمحتويات
// من علامة المستند المنظم هذه لتمتد على سطر واحد.
// قم بضبط خاصية "متعدد الأسطر" على "true" للسماح للعلامة باحتواء أسطر متعددة من المحتوى.
tag.Multiline = true;

// قم بتعيين خاصية "المظهر" إلى "SdtAppearance.Tags" لإظهار العلامات حول المحتوى.
 // بشكل افتراضي، يظهر علامة المستند المنظم على هيئة BoundingBox.
tag.Appearance = SdtAppearance.Tags;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(tag);

// قم بإدراج نسخة من علامة المستند المنظم لدينا في فقرة جديدة.
StructuredDocumentTag tagClone = (StructuredDocumentTag)tag.Clone(true);
builder.InsertParagraph();
builder.InsertNode(tagClone);

// استخدم طريقة "RemoveSelfOnly" لإزالة علامة مستند منظمة، مع الاحتفاظ بمحتوياتها في المستند.
tagClone.RemoveSelfOnly();

doc.Save(ArtifactsDir + "StructuredDocumentTag.PlainText.docx");
```

### أنظر أيضا

* class [Font](../../../aspose.words/font/)
* class [StructuredDocumentTag](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
