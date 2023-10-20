---
title: FormField.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words لـ .NET
description: FormField Name ملكية. الحصول على اسم حقل النموذج أو تعيينه في C#.
type: docs
weight: 130
url: /ar/net/aspose.words.fields/formfield/name/
---
## FormField.Name property

الحصول على اسم حقل النموذج أو تعيينه.

```csharp
public string Name { get; set; }
```

## ملاحظات

يسمح Microsoft Word بالسلاسل التي تحتوي على 20 حرفًا على الأكثر.

## أمثلة

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

* class [FormField](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
