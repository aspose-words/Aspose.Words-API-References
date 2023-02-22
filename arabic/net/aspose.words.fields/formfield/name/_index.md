---
title: FormField.Name
second_title: Aspose.Words لمراجع .NET API
description: FormField ملكية. الحصول على اسم حقل النموذج أو تعيينه.
type: docs
weight: 130
url: /ar/net/aspose.words.fields/formfield/name/
---
## FormField.Name property

الحصول على اسم حقل النموذج أو تعيينه.

```csharp
public string Name { get; set; }
```

### ملاحظات

يسمح Microsoft Word بالسلاسل التي تحتوي على 20 حرفًا بحد أقصى.

### أمثلة

يوضح كيفية إدراج مربع تحرير وسرد.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// أدخل مربع تحرير وسرد يسمح للمستخدم باختيار خيار من مجموعة سلاسل.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

Assert.AreEqual("MyComboBox", comboBox.Name);
Assert.AreEqual(FieldType.FieldFormDropDown, comboBox.Type);
Assert.AreEqual("Apple", comboBox.Result);

// سيظهر حقل النموذج في شكل علامة html "تحديد".
doc.Save(ArtifactsDir + "FormFields.Create.html");
```

### أنظر أيضا

* class [FormField](../)
* مساحة الاسم [Aspose.Words.Fields](../../formfield/)
* المجسم [Aspose.Words](../../../)


