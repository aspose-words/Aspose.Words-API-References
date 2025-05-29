---
title: FormField.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية إدارة خاصية FormField Name بسهولة لتخصيص نماذجك وتحسينها لتحقيق تفاعل أفضل للمستخدمين وجمع البيانات.
type: docs
weight: 130
url: /ar/net/aspose.words.fields/formfield/name/
---
## FormField.Name property

يحصل على اسم حقل النموذج أو يعينه.

```csharp
public string Name { get; set; }
```

## ملاحظات

يسمح Microsoft Word باستخدام سلاسل تحتوي على 20 حرفًا كحد أقصى.

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

* class [FormField](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
