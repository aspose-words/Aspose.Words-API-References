---
title: VariableCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words لـ .NET
description: VariableCollection Add طريقة. إضافة متغير مستند إلى المجموعة في C#.
type: docs
weight: 30
url: /ar/net/aspose.words/variablecollection/add/
---
## VariableCollection.Add method

إضافة متغير مستند إلى المجموعة.

```csharp
public void Add(string name, string value)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| name | String | الاسم غير حساس لحالة الأحرف للمتغير المراد إضافته. |
| value | String | قيمة المتغير. لا يمكن أن تكون القيمة`باطل`، إذا كانت القيمة فارغة فسيتم استخدام سلسلة فارغة بدلاً من ذلك. |

## أمثلة

يوضح كيفية العمل مع مجموعة متغيرات المستند.

```csharp
Document doc = new Document();
VariableCollection variables = doc.Variables;

// يحتوي كل مستند على مجموعة من متغيرات زوج المفتاح/القيمة، والتي يمكننا إضافة عناصر إليها.
variables.Add("Home address", "123 Main St.");
variables.Add("City", "London");
variables.Add("Bedrooms", "3");

Assert.AreEqual(3, variables.Count);

// يمكننا عرض قيم المتغيرات في نص الوثيقة باستخدام حقول DOCVARIABLE.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocVariable field = (FieldDocVariable)builder.InsertField(FieldType.FieldDocVariable, true);
field.VariableName = "Home address";
field.Update();

Assert.AreEqual("123 Main St.", field.Result);

// سيؤدي تعيين القيم للمفاتيح الموجودة إلى تحديثها.
variables.Add("Home address", "456 Queen St.");

// سيتعين علينا بعد ذلك تحديث حقول DOCVARIABLE للتأكد من أنها تعرض قيمة محدثة.
Assert.AreEqual("123 Main St.", field.Result);

field.Update();

Assert.AreEqual("456 Queen St.", field.Result);

// التحقق من وجود متغيرات المستند ذات اسم أو قيمة معينة.
Assert.True(variables.Contains("City"));
Assert.True(variables.Any(v => v.Value == "London"));

// تقوم مجموعة المتغيرات بفرز المتغيرات أبجديًا حسب الاسم تلقائيًا.
Assert.AreEqual(0, variables.IndexOfKey("Bedrooms"));
Assert.AreEqual(1, variables.IndexOfKey("City"));
Assert.AreEqual(2, variables.IndexOfKey("Home address"));

// تعداد مجموعة المتغيرات.
using (IEnumerator<KeyValuePair<string, string>> enumerator = doc.Variables.GetEnumerator())
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: {enumerator.Current.Key}, Value: {enumerator.Current.Value}");

// فيما يلي ثلاث طرق لإزالة متغيرات المستند من المجموعة.
// 1 - بالاسم:
variables.Remove("City");

Assert.False(variables.Contains("City"));

// 2 - حسب الفهرس:
variables.RemoveAt(1);

Assert.False(variables.Contains("Home address"));

// 3 - مسح المجموعة بأكملها مرة واحدة:
variables.Clear();

Assert.That(variables, Is.Empty);
```

### أنظر أيضا

* class [VariableCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
