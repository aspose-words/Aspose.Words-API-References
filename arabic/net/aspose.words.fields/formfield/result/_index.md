---
title: FormField.Result
linktitle: Result
articleTitle: Result
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FormField Result، وقم بإدارة وتخصيص إخراج السلسلة لحقول النموذج بسهولة لتحسين تجربة المستخدم.
type: docs
weight: 170
url: /ar/net/aspose.words.fields/formfield/result/
---
## FormField.Result property

يحصل على سلسلة تمثل نتيجة حقل النموذج هذا أو يعينها.

```csharp
public string Result { get; set; }
```

## ملاحظات

بالنسبة لحقل نموذج النص، النتيجة هي النص الموجود في الحقل.

بالنسبة لحقل نموذج مربع الاختيار، يمكن أن تكون النتيجة "1" أو "0" للإشارة إلى التحديد أو عدم التحديد.

بالنسبة لحقل نموذج القائمة المنسدلة، تكون النتيجة هي السلسلة المحددة في القائمة المنسدلة.

جلسة`Result` بالنسبة لحقل نموذج النص، لا يتم تطبيق تنسيق النص المحدد في[`TextInputFormat`](../textinputformat/) إذا كنت تريد تعيين قيمة وتطبيق تنسيق ، فاستخدم[`SetTextInputValue`](../settextinputvalue/) طريقة.

بالنسبة لحقل نموذج النص،[`TextInputDefault`](../textinputdefault/) القيمة يتم تطبيقها إذا*value* يكون`باطل`.

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
