---
title: VariableCollection Class
linktitle: VariableCollection
articleTitle: VariableCollection
second_title: Aspose.Words لـ .NET
description: Aspose.Words.VariableCollection فصل. مجموعة من متغيرات الوثيقة في C#.
type: docs
weight: 6530
url: /ar/net/aspose.words/variablecollection/
---
## VariableCollection class

مجموعة من متغيرات الوثيقة.

لمعرفة المزيد، قم بزيارة[العمل مع خصائص الوثيقة](https://docs.aspose.com/words/net/work-with-document-properties/) مقالة توثيقية.

```csharp
public class VariableCollection : IEnumerable<KeyValuePair<string, string>>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words/variablecollection/count/) { get; } | الحصول على عدد العناصر الموجودة في المجموعة. |
| [Item](../../aspose.words/variablecollection/item/) { get; set; } | الحصول على متغير مستند أو تعيينه باستخدام اسم غير حساس لحالة الأحرف. `باطل` لا يُسمح بالقيم في الجانب الأيمن من المهمة وسيتم استبدالها بسلسلة فارغة. (2 indexers) |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words/variablecollection/add/)(*string, string*) | إضافة متغير مستند إلى المجموعة. |
| [Clear](../../aspose.words/variablecollection/clear/)() | إزالة كافة العناصر من المجموعة. |
| [Contains](../../aspose.words/variablecollection/contains/)(*string*) | تحديد ما إذا كانت المجموعة تحتوي على متغير مستند بالاسم المحدد. |
| [GetEnumerator](../../aspose.words/variablecollection/getenumerator/)() | يُرجع كائن العداد الذي يمكن استخدامه للتكرار على كافة المتغيرات في المجموعة. |
| [IndexOfKey](../../aspose.words/variablecollection/indexofkey/)(*string*) | إرجاع الفهرس الصفري لمتغير المستند المحدد في المجموعة. |
| [Remove](../../aspose.words/variablecollection/remove/)(*string*) | إزالة متغير مستند بالاسم المحدد من المجموعة. |
| [RemoveAt](../../aspose.words/variablecollection/removeat/)(*int*) | إزالة متغير مستند في الفهرس المحدد. |

## ملاحظات

أسماء وقيم المتغيرات هي سلاسل.

أسماء المتغيرات غير حساسة لحالة الأحرف.

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

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
