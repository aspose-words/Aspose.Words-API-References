---
title: FormField.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FormField Type لتتمكن من التعرف بسهولة على أنواع حقول النماذج المختلفة والاستفادة منها، مما يعزز وظائف نماذج الويب لديك وتجربة المستخدم.
type: docs
weight: 220
url: /ar/net/aspose.words.fields/formfield/type/
---
## FormField.Type property

يعيد نوع حقل النموذج.

```csharp
public FieldType Type { get; }
```

## أمثلة

يوضح كيفية إدراج مربع المجموعة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// أدخل مربعًا مركبًا يسمح للمستخدم باختيار خيار من مجموعة من السلاسل.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

Assert.AreEqual("MyComboBox", comboBox.Name);
Assert.AreEqual(FieldType.FieldFormDropDown, comboBox.Type);
Assert.AreEqual("Apple", comboBox.Result);

//سيظهر حقل النموذج في شكل علامة HTML "select".
doc.Save(ArtifactsDir + "FormFields.Create.html");
```

### أنظر أيضا

* enum [FieldType](../../fieldtype/)
* class [FormField](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
