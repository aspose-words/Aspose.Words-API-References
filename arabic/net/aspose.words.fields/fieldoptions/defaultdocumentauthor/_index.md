---
title: FieldOptions.DefaultDocumentAuthor
linktitle: DefaultDocumentAuthor
articleTitle: DefaultDocumentAuthor
second_title: Aspose.Words لـ .NET
description: FieldOptions DefaultDocumentAuthor ملكية. الحصول على أو تعيين اسم مؤلف المستند الافتراضي. إذا كان اسم المؤلف محددًا بالفعل في خصائص المستند المضمنة فلن يتم أخذ هذا الخيار في الاعتبار في C#.
type: docs
weight: 70
url: /ar/net/aspose.words.fields/fieldoptions/defaultdocumentauthor/
---
## FieldOptions.DefaultDocumentAuthor property

الحصول على أو تعيين اسم مؤلف المستند الافتراضي. إذا كان اسم المؤلف محددًا بالفعل في خصائص المستند المضمنة، فلن يتم أخذ هذا الخيار في الاعتبار.

```csharp
public string DefaultDocumentAuthor { get; set; }
```

## أمثلة

يوضح كيفية استخدام حقل المؤلف لعرض اسم منشئ المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// حقول المؤلف مصدر نتائجها من خاصية المستند المضمنة والتي تسمى "المؤلف".
// إذا قمنا بإنشاء مستند وحفظه في برنامج Microsoft Word،
// سيكون له اسم المستخدم الخاص بنا في تلك الخاصية.
// ومع ذلك، إذا قمنا بإنشاء مستند برمجيًا باستخدام Aspose.Words،
// ستكون خاصية "المؤلف" سلسلة فارغة بشكل افتراضي.
Assert.AreEqual(string.Empty, doc.BuiltInDocumentProperties.Author);

// قم بتعيين اسم مؤلف احتياطي لحقول المؤلف لاستخدامها
// إذا كانت خاصية "المؤلف" تحتوي على سلسلة فارغة.
doc.FieldOptions.DefaultDocumentAuthor = "Joe Bloggs";

builder.Write("This document was created by ");
FieldAuthor field = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("Joe Bloggs", field.Result);

// تحديث حقل المؤلف الذي يحتوي على قيمة
// سيتم تطبيق هذه القيمة على خاصية "المؤلف" المضمنة.
Assert.AreEqual("Joe Bloggs", doc.BuiltInDocumentProperties.Author);

// سيؤدي تغيير هذه الخاصية ثم تحديث حقل المؤلف إلى تطبيق هذه القيمة على الحقل.
doc.BuiltInDocumentProperties.Author = "John Doe";      
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("John Doe", field.Result);

// إذا قمنا بتحديث حقل المؤلف بعد تغيير خاصية "الاسم" الخاصة به،
// ثم سيعرض الحقل الاسم الجديد ويطبق الاسم الجديد على الخاصية المضمنة.
field.AuthorName = "Jane Doe";
field.Update();

Assert.AreEqual(" AUTHOR  \"Jane Doe\"", field.GetFieldCode());
Assert.AreEqual("Jane Doe", field.Result);

// حقول المؤلف لا تؤثر على خاصية DefaultDocumentAuthor.
Assert.AreEqual("Jane Doe", doc.BuiltInDocumentProperties.Author);
Assert.AreEqual("Joe Bloggs", doc.FieldOptions.DefaultDocumentAuthor);

doc.Save(ArtifactsDir + "Field.AUTHOR.docx");
```

### أنظر أيضا

* class [FieldOptions](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
