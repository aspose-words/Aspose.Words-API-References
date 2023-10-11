---
title: FormField.Type
second_title: Aspose.Words لمراجع .NET API
description: FormField ملكية. إرجاع نوع حقل النموذج.
type: docs
weight: 220
url: /ar/net/aspose.words.fields/formfield/type/
---
## FormField.Type property

إرجاع نوع حقل النموذج.

```csharp
public FieldType Type { get; }
```

### أمثلة

يوضح كيفية إدراج مربع التحرير والسرد.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// أدخل مربع التحرير والسرد الذي سيسمح للمستخدم باختيار خيار من مجموعة من السلاسل.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

Assert.AreEqual("MyComboBox", comboBox.Name);
Assert.AreEqual(FieldType.FieldFormDropDown, comboBox.Type);
Assert.AreEqual("Apple", comboBox.Result);

// سيظهر حقل النموذج على شكل علامة html "تحديد".
doc.Save(ArtifactsDir + "FormFields.Create.html");
```

### أنظر أيضا

* enum [FieldType](../../fieldtype/)
* class [FormField](../)
* مساحة الاسم [Aspose.Words.Fields](../../formfield/)
* المجسم [Aspose.Words](../../../)


