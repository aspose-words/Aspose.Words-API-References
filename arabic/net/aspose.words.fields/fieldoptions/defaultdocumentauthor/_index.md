---
title: FieldOptions.DefaultDocumentAuthor
linktitle: DefaultDocumentAuthor
articleTitle: DefaultDocumentAuthor
second_title: Aspose.Words لـ .NET
description: إدارة خاصية DefaultDocumentAuthor لتعيين أسماء مؤلفي المستندات أو تحديثها بسهولة، مما يعزز كفاءة التنظيم وإدارة المستندات.
type: docs
weight: 70
url: /ar/net/aspose.words.fields/fieldoptions/defaultdocumentauthor/
---
## FieldOptions.DefaultDocumentAuthor property

يحصل على اسم مؤلف المستند الافتراضي أو يعيّنه. إذا كان اسم المؤلف محددًا مسبقًا في خصائص المستند المضمنة، فلن يُؤخذ هذا الخيار في الاعتبار.

```csharp
public string DefaultDocumentAuthor { get; set; }
```

## أمثلة

يوضح كيفية استخدام حقل المؤلف لعرض اسم منشئ المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تحصل حقول المؤلف على نتائجها من خاصية المستند المضمنة المسماة "المؤلف".
// إذا قمنا بإنشاء مستند وحفظه في Microsoft Word،
//سيكون اسم المستخدم الخاص بنا موجودًا في تلك الخاصية.
// ومع ذلك، إذا قمنا بإنشاء مستند برمجيًا باستخدام Aspose.Words،
// ستكون خاصية "المؤلف"، بشكل افتراضي، عبارة عن سلسلة فارغة.
Assert.AreEqual(string.Empty, doc.BuiltInDocumentProperties.Author);

// تعيين اسم مؤلف احتياطي لحقول المؤلف لاستخدامه
// إذا كانت خاصية "المؤلف" تحتوي على سلسلة فارغة.
doc.FieldOptions.DefaultDocumentAuthor = "Joe Bloggs";

builder.Write("This document was created by ");
FieldAuthor field = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("Joe Bloggs", field.Result);

// تحديث حقل AUTHOR الذي يحتوي على قيمة
// سيتم تطبيق هذه القيمة على الخاصية المضمنة "المؤلف".
Assert.AreEqual("Joe Bloggs", doc.BuiltInDocumentProperties.Author);

// سيؤدي تغيير هذه الخاصية، ثم تحديث حقل AUTHOR، إلى تطبيق هذه القيمة على الحقل.
doc.BuiltInDocumentProperties.Author = "John Doe";
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("John Doe", field.Result);

// إذا قمنا بتحديث حقل AUTHOR بعد تغيير خاصية "Name" الخاصة به،
// ثم سيعرض الحقل الاسم الجديد وسيطبق الاسم الجديد على الخاصية المضمنة.
field.AuthorName = "Jane Doe";
field.Update();

Assert.AreEqual(" AUTHOR  \"Jane Doe\"", field.GetFieldCode());
Assert.AreEqual("Jane Doe", field.Result);

// لا تؤثر حقول AUTHOR على خاصية DefaultDocumentAuthor.
Assert.AreEqual("Jane Doe", doc.BuiltInDocumentProperties.Author);
Assert.AreEqual("Joe Bloggs", doc.FieldOptions.DefaultDocumentAuthor);

doc.Save(ArtifactsDir + "Field.AUTHOR.docx");
```

### أنظر أيضا

* class [FieldOptions](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
