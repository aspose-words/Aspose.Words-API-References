---
title: VariableCollection.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words لـ .NET
description: امسح جميع عناصر مجموعة المتغيرات الخاصة بك بسهولة باستخدام طريقة المسح لدينا. بسّط إدارة بياناتك اليوم!
type: docs
weight: 40
url: /ar/net/aspose.words/variablecollection/clear/
---
## VariableCollection.Clear method

يزيل جميع العناصر من المجموعة.

```csharp
public void Clear()
```

## أمثلة

يوضح كيفية العمل مع مجموعة المتغيرات الخاصة بالمستند.

```csharp
Document doc = new Document();
VariableCollection variables = doc.Variables;

// تحتوي كل وثيقة على مجموعة من متغيرات أزواج المفتاح/القيمة، والتي يمكننا إضافة عناصر إليها.
variables.Add("Home address", "123 Main St.");
variables.Add("City", "London");
variables.Add("Bedrooms", "3");

Assert.AreEqual(3, variables.Count);

//يمكننا عرض قيم المتغيرات في نص المستند باستخدام حقول DOCVARIABLE.
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

// تأكد من وجود متغيرات المستند التي تحمل اسمًا أو قيمة معينة.
Assert.True(variables.Contains("City"));
Assert.True(variables.Any(v => v.Value == "London"));

// تقوم مجموعة المتغيرات بفرز المتغيرات أبجديًا حسب الاسم تلقائيًا.
Assert.AreEqual(0, variables.IndexOfKey("Bedrooms"));
Assert.AreEqual(1, variables.IndexOfKey("City"));
Assert.AreEqual(2, variables.IndexOfKey("Home address"));

Assert.AreEqual("3", variables[0]);
Assert.AreEqual("London", variables["City"]);

//إحصاء مجموعة المتغيرات.
using (IEnumerator<KeyValuePair<string, string>> enumerator = doc.Variables.GetEnumerator())
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: {enumerator.Current.Key}, Value: {enumerator.Current.Value}");

// فيما يلي ثلاث طرق لإزالة متغيرات المستند من المجموعة.
// 1 - حسب الاسم:
variables.Remove("City");

Assert.False(variables.Contains("City"));

// 2 - حسب الفهرس:
variables.RemoveAt(1);

Assert.False(variables.Contains("Home address"));

// 3 - مسح المجموعة بأكملها مرة واحدة:
variables.Clear();

Assert.AreEqual(0, variables.Count);
```

### أنظر أيضا

* class [VariableCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
