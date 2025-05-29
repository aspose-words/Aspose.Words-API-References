---
title: FieldAuthor.AuthorName
linktitle: AuthorName
articleTitle: AuthorName
second_title: Aspose.Words لـ .NET
description: أدر مؤلفي المستندات بسهولة باستخدام FieldAuthor AuthorName. احصل على أسماء المؤلفين أو عيّنها بسهولة لتعزيز مصداقية محتواك وتنظيمه.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldauthor/authorname/
---
## FieldAuthor.AuthorName property

يحصل على اسم مؤلف المستند أو يعينه.

```csharp
public string AuthorName { get; set; }
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

* class [FieldAuthor](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
