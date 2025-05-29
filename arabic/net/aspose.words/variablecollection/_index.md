---
title: VariableCollection Class
linktitle: VariableCollection
articleTitle: VariableCollection
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.VariableCollection، وقم بإدارة وتخصيص متغيرات المستندات بكفاءة لتحسين أتمتة المستندات ومرونتها.
type: docs
weight: 7380
url: /ar/net/aspose.words/variablecollection/
---
## VariableCollection class

مجموعة من متغيرات المستند.

لمعرفة المزيد، قم بزيارة[العمل مع خصائص المستند](https://docs.aspose.com/words/net/work-with-document-properties/) مقالة توثيقية.

```csharp
public class VariableCollection : IEnumerable<KeyValuePair<string, string>>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words/variablecollection/count/) { get; } | يحصل على عدد العناصر الموجودة في المجموعة. |
| [Item](../../aspose.words/variablecollection/item/) { get; set; } | يحصل على متغير مستند أو يعينه حسب الاسم غير الحساس لحالة الأحرف. `باطل`لا يُسمح بالقيم على الجانب الأيمن من التعيين وسيتم استبدالها بسلسلة فارغة. (2 indexers) |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words/variablecollection/add/)(*string, string*) | يضيف متغير مستند إلى المجموعة. |
| [Clear](../../aspose.words/variablecollection/clear/)() | يزيل جميع العناصر من المجموعة. |
| [Contains](../../aspose.words/variablecollection/contains/)(*string*) | يحدد ما إذا كانت المجموعة تحتوي على متغير مستند يحمل الاسم المحدد. |
| [GetEnumerator](../../aspose.words/variablecollection/getenumerator/)() | يعيد كائن عداد يمكن استخدامه للتكرار على جميع المتغيرات في المجموعة. |
| [IndexOfKey](../../aspose.words/variablecollection/indexofkey/)(*string*) | يعيد الفهرس الصفري للمتغير المستند المحدد في المجموعة. |
| [Remove](../../aspose.words/variablecollection/remove/)(*string*) | يزيل متغير المستند بالاسم المحدد من المجموعة. |
| [RemoveAt](../../aspose.words/variablecollection/removeat/)(*int*) | يزيل متغير المستند عند الفهرس المحدد. |

## ملاحظات

أسماء المتغيرات والقيم عبارة عن سلاسل.

أسماء المتغيرات لا تميز بين الأحرف الكبيرة والصغيرة.

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

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
