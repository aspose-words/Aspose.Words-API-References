---
title: FormField.Result
second_title: Aspose.Words لمراجع .NET API
description: FormField ملكية. الحصول على أو تعيين سلسلة تمثل نتيجة حقل النموذج هذا.
type: docs
weight: 170
url: /ar/net/aspose.words.fields/formfield/result/
---
## FormField.Result property

الحصول على أو تعيين سلسلة تمثل نتيجة حقل النموذج هذا.

```csharp
public string Result { get; set; }
```

### ملاحظات

بالنسبة لحقل نموذج النص، تكون النتيجة هي النص الموجود في الحقل.

بالنسبة لحقل نموذج خانة الاختيار، يمكن أن تكون النتيجة "1" أو "0" للإشارة إلى أنه محدد أو غير محدد.

بالنسبة لحقل نموذج القائمة المنسدلة، تكون النتيجة هي السلسلة المحددة في القائمة المنسدلة.

جلسة`Result` لحقل نموذج النص لا يطبق تنسيق النص المحدد في[`TextInputFormat`](../textinputformat/) . إذا كنت تريد تعيين قيمة وتطبيق تنسيق ، فاستخدم الملف[`SetTextInputValue`](../settextinputvalue/) طريقة.

بالنسبة لحقل نموذج نصي[`TextInputDefault`](../textinputdefault/) يتم تطبيق القيمة إذا*value* يكون`باطل`.

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

* class [FormField](../)
* مساحة الاسم [Aspose.Words.Fields](../../formfield/)
* المجسم [Aspose.Words](../../../)


