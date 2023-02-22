---
title: VariableCollection.Count
second_title: Aspose.Words لمراجع .NET API
description: VariableCollection ملكية. الحصول على عدد العناصر الموجودة في المجموعة.
type: docs
weight: 10
url: /ar/net/aspose.words/variablecollection/count/
---
## VariableCollection.Count property

الحصول على عدد العناصر الموجودة في المجموعة.

```csharp
public int Count { get; }
```

### أمثلة

يوضح كيفية العمل مع مجموعة متغيرات المستند.

```csharp
Document doc = new Document();
VariableCollection variables = doc.Variables;

// يحتوي كل مستند على مجموعة من متغيرات زوج المفتاح / القيمة ، والتي يمكننا إضافة عناصر إليها.
variables.Add("Home address", "123 Main St.");
variables.Add("City", "London");
variables.Add("Bedrooms", "3");

Assert.AreEqual(3, variables.Count);

// يمكننا عرض قيم المتغيرات في نص المستند باستخدام حقول DOCVARIABLE.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocVariable field = (FieldDocVariable)builder.InsertField(FieldType.FieldDocVariable, true);
field.VariableName = "Home address";
field.Update();

Assert.AreEqual("123 Main St.", field.Result);

// سيؤدي تعيين قيم للمفاتيح الموجودة إلى تحديثها.
variables.Add("Home address", "456 Queen St.");

// سيتعين علينا بعد ذلك تحديث حقول DOCVARIABLE للتأكد من أنها تعرض قيمة محدثة.
Assert.AreEqual("123 Main St.", field.Result);

field.Update();

Assert.AreEqual("456 Queen St.", field.Result);

// تحقق من وجود متغيرات المستند باسم أو قيمة معينة.
Assert.True(variables.Contains("City"));
Assert.True(variables.Any(v => v.Value == "London"));

// تقوم مجموعة المتغيرات تلقائيًا بفرز المتغيرات أبجديًا بالاسم.
Assert.AreEqual(0, variables.IndexOfKey("Bedrooms"));
Assert.AreEqual(1, variables.IndexOfKey("City"));
Assert.AreEqual(2, variables.IndexOfKey("Home address"));

// عد على مجموعة المتغيرات.
using (IEnumerator<KeyValuePair<string, string>> enumerator = doc.Variables.GetEnumerator())
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: {enumerator.Current.Key}, Value: {enumerator.Current.Value}");

// فيما يلي ثلاث طرق لإزالة متغيرات المستند من مجموعة.
// 1 - بالاسم:
variables.Remove("City");

Assert.False(variables.Contains("City"));

// 2 - حسب الفهرس:
variables.RemoveAt(1);

Assert.False(variables.Contains("Home address"));

// 3 - امسح المجموعة بأكملها مرة واحدة:
variables.Clear();

Assert.That(variables, Is.Empty);
```

### أنظر أيضا

* class [VariableCollection](../)
* مساحة الاسم [Aspose.Words](../../variablecollection/)
* المجسم [Aspose.Words](../../../)


