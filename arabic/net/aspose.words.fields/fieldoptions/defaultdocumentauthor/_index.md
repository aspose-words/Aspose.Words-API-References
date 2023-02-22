---
title: FieldOptions.DefaultDocumentAuthor
second_title: Aspose.Words لمراجع .NET API
description: FieldOptions ملكية. الحصول على أو تعيين اسم مؤلف المستند الافتراضي. إذا كان اسم المؤلف محددًا بالفعل في خصائص المستند المضمنة  فلن يتم اعتبار هذا الخيار .
type: docs
weight: 60
url: /ar/net/aspose.words.fields/fieldoptions/defaultdocumentauthor/
---
## FieldOptions.DefaultDocumentAuthor property

الحصول على أو تعيين اسم مؤلف المستند الافتراضي. إذا كان اسم المؤلف محددًا بالفعل في خصائص المستند المضمنة ، فلن يتم اعتبار هذا الخيار .

```csharp
public string DefaultDocumentAuthor { get; set; }
```

### أمثلة

يوضح كيفية استخدام حقل AUTHOR لعرض اسم منشئ المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// مصدر الحقول AUTHOR هو نتائجها من خاصية المستند المضمنة التي تسمى "المؤلف".
// إذا أنشأنا مستندًا وحفظناه في Microsoft Word ،
// سيكون لها اسم المستخدم الخاص بنا في تلك الخاصية.
// ومع ذلك ، إذا أنشأنا مستندًا برمجيًا باستخدام Aspose.Words ،
 // ستكون خاصية "المؤلف" ، افتراضيًا ، سلسلة فارغة.
Assert.AreEqual(string.Empty, doc.BuiltInDocumentProperties.Author);

// تعيين اسم مؤلف احتياطي لحقول AUTHOR المراد استخدامها
// إذا كانت خاصية "المؤلف" تحتوي على سلسلة فارغة.
doc.FieldOptions.DefaultDocumentAuthor = "Joe Bloggs";

builder.Write("This document was created by ");
FieldAuthor field = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("Joe Bloggs", field.Result);

// تحديث حقل AUTHOR يحتوي على قيمة
// سيطبق هذه القيمة على خاصية "المؤلف" المضمنة.
Assert.AreEqual("Joe Bloggs", doc.BuiltInDocumentProperties.Author);

// سيؤدي تغيير هذه الخاصية ، ثم تحديث حقل AUTHOR إلى تطبيق هذه القيمة على الحقل.
doc.BuiltInDocumentProperties.Author = "John Doe";      
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("John Doe", field.Result);

// إذا قمنا بتحديث حقل AUTHOR بعد تغيير خاصية "الاسم" الخاصة به ،
// ثم سيعرض الحقل الاسم الجديد ويطبق الاسم الجديد على الخاصية المضمنة.
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
* مساحة الاسم [Aspose.Words.Fields](../../fieldoptions/)
* المجسم [Aspose.Words](../../../)


