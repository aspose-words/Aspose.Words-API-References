---
title: StructuredDocumentTag.Id
second_title: Aspose.Words لمراجع .NET API
description: StructuredDocumentTag ملكية. يحدد معرّفًا رقميًا فريدًا ومستمرًا للقراءة فقط لهذا الغرض المعاملة الخاصة والتفضيلية.
type: docs
weight: 140
url: /ar/net/aspose.words.markup/structureddocumenttag/id/
---
## StructuredDocumentTag.Id property

يحدد معرّفًا رقميًا فريدًا ومستمرًا للقراءة فقط لهذا الغرض **المعاملة الخاصة والتفضيلية**.

```csharp
public int Id { get; }
```

### ملاحظات

يجب أن تتبع سمة المعرّف القواعد التالية:

* يجب أن تحتفظ الوثيقة بمعرفات المعاملة الخاصة والتفضيلية فقط إذا تم نسخ الوثيقة بأكملها[`Clone`](../../../aspose.words/document/clone/).
* أثناء[`ImportNode`](../../../aspose.words/documentbase/importnode/) يجب الاحتفاظ بالمعرف إذا لم يتسبب الاستيراد في تعارض مع معرفات SDT الأخرى في المستند الهدف.
* إذا حددت عدة عُقد SDT نفس قيمة الرقم العشري لسمة المعرّف ، عندئذٍ يجب أن تحتفظ SDT الأول في المستند بهذا المعرّف الأصلي ، ويجب أن يكون لجميع عُقد SDT اللاحقة معرّفات جديدة مخصصة لها عند تحميل المستند.
* أثناء المعاملة الخاصة والتفضيلية المستقلةINodeCloningListener) سيتم إنشاء معرّف فريد جديد للعملية لعقدة المعاملة الخاصة والتفضيلية المستنسخة.
* إذا لم يتم تحديد المعرف في المستند المصدر ، فيجب أن يكون لعقدة SDT معرفًا فريدًا جديدًا يتم تعيينه لها عند تحميل المستند.

### أمثلة

يوضح كيفية إنشاء علامة وثيقة منظمة في مربع نص عادي وتعديل مظهره.

```csharp
Document doc = new Document();

// إنشاء علامة وثيقة منظمة تحتوي على نص عادي.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// قم بتعيين عنوان ولون الإطار الذي يظهر عند تحريك الماوس فوق علامة المستند المهيكلة في Microsoft Word.
tag.Title = "My plain text";
tag.Color = Color.Magenta;

// تعيين علامة لعلامة المستند المنظمة هذه ، والتي يمكن الحصول عليها
// كعنصر XML يسمى "tag" ، مع السلسلة الموجودة أدناه في سمة "val" الخاصة بها.
tag.Tag = "MyPlainTextSDT";

// كل علامة وثيقة منظمة لها معرّف فريد عشوائي.
Assert.That(tag.Id, Is.Positive);

// تعيين خط النص داخل علامة المستند المهيكل.
tag.ContentsFont.Name = "Arial";

// تعيين خط النص في نهاية علامة المستند المهيكل.
// أي نص نكتبه في نص المستند بعد الخروج من العلامة باستخدام مفاتيح الأسهم سيستخدم هذا الخط.
tag.EndCharacterFont.Name = "Arial Black";

// بشكل افتراضي ، هذا خطأ والضغط على مفتاح الإدخال أثناء وجوده داخل علامة مستند منظم لا يفعل شيئًا.
// عند التعيين على "صحيح" ، يمكن أن تحتوي علامة المستند المهيكلة الخاصة بنا على عدة أسطر.

// اضبط خاصية "Multiline" على "false" للسماح فقط بالمحتويات
// من علامة المستند المهيكلة هذه لتمتد إلى سطر واحد.
// اضبط خاصية "Multiline" على "true" للسماح للعلامة بأن تحتوي على أسطر متعددة من المحتوى.
tag.Multiline = true;

// عيّن خاصية "Appearance" على "SdtAppearance.Tags" لإظهار العلامات حول المحتوى.
 // بشكل افتراضي تظهر علامة المستند المهيكلة على أنها BoundingBox.
tag.Appearance = SdtAppearance.Tags;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(tag);

// أدخل نسخة من علامة المستند المهيكلة الخاصة بنا في فقرة جديدة.
StructuredDocumentTag tagClone = (StructuredDocumentTag)tag.Clone(true);
builder.InsertParagraph();
builder.InsertNode(tagClone);

// استخدم طريقة "RemoveSelfOnly" لإزالة علامة مستند منظم ، مع الاحتفاظ بمحتوياتها في المستند.
tagClone.RemoveSelfOnly();

doc.Save(ArtifactsDir + "StructuredDocumentTag.PlainText.docx");
```

### أنظر أيضا

* class [StructuredDocumentTag](../)
* مساحة الاسم [Aspose.Words.Markup](../../structureddocumenttag/)
* المجسم [Aspose.Words](../../../)


