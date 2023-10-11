---
title: Class DropDownItemCollection
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Fields.DropDownItemCollection فصل. مجموعة من السلاسل التي تمثل كافة العناصر الموجودة في حقل النموذج المنسدل.
type: docs
weight: 1500
url: /ar/net/aspose.words.fields/dropdownitemcollection/
---
## DropDownItemCollection class

مجموعة من السلاسل التي تمثل كافة العناصر الموجودة في حقل النموذج المنسدل.

لمعرفة المزيد، قم بزيارة[العمل مع الحقول](https://docs.aspose.com/words/net/working-with-fields/) مقالة توثيقية.

```csharp
public class DropDownItemCollection : IEnumerable<string>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words.fields/dropdownitemcollection/count/) { get; } | الحصول على عدد العناصر الموجودة في المجموعة. |
| [Item](../../aspose.words.fields/dropdownitemcollection/item/) { get; set; } | الحصول على العنصر أو تعيينه في الفهرس المحدد. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words.fields/dropdownitemcollection/add/)(string) | إضافة سلسلة إلى نهاية المجموعة. |
| [Clear](../../aspose.words.fields/dropdownitemcollection/clear/)() | إزالة كافة العناصر من المجموعة. |
| [Contains](../../aspose.words.fields/dropdownitemcollection/contains/)(string) | تحديد ما إذا كانت المجموعة تحتوي على القيمة المحددة. |
| [GetEnumerator](../../aspose.words.fields/dropdownitemcollection/getenumerator/)() | إرجاع كائن العداد الذي يمكن استخدامه للتكرار على كافة العناصر الموجودة في المجموعة. |
| [IndexOf](../../aspose.words.fields/dropdownitemcollection/indexof/)(string) | إرجاع الفهرس الصفري للقيمة المحددة في المجموعة. |
| [Insert](../../aspose.words.fields/dropdownitemcollection/insert/)(int, string) | إدراج سلسلة في المجموعة في الفهرس المحدد. |
| [Remove](../../aspose.words.fields/dropdownitemcollection/remove/)(string) | إزالة القيمة المحددة من المجموعة. |
| [RemoveAt](../../aspose.words.fields/dropdownitemcollection/removeat/)(int) | إزالة قيمة في الفهرس المحدد. |

### أمثلة

يوضح كيفية إدراج حقل مربع التحرير والسرد، وتحرير العناصر الموجودة في مجموعة العناصر الخاصة به.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإدراج مربع التحرير والسرد، ثم تحقق من مجموعته من العناصر المنسدلة.
// في Microsoft Word، سيقوم المستخدم بالنقر فوق مربع التحرير والسرد،
// ثم اختر أحد عناصر النص في المجموعة لعرضه.
string[] items = { "One", "Two", "Three" };
FormField comboBoxField = builder.InsertComboBox("DropDown", items, 0);
DropDownItemCollection dropDownItems = comboBoxField.DropDownItems;

Assert.AreEqual(3, dropDownItems.Count);
Assert.AreEqual("One", dropDownItems[0]);
Assert.AreEqual(1, dropDownItems.IndexOf("Two"));
Assert.IsTrue(dropDownItems.Contains("Three"));

// هناك طريقتان لإضافة عنصر جديد إلى مجموعة موجودة من عناصر المربع المنسدل.
// 1 - إلحاق عنصر بنهاية المجموعة:
dropDownItems.Add("Four");

// 2 - إدراج عنصر قبل عنصر آخر في فهرس محدد:
dropDownItems.Insert(3, "Three and a half");

Assert.AreEqual(5, dropDownItems.Count);

// كرر المجموعة واطبع كل عنصر.
using (IEnumerator<string> dropDownCollectionEnumerator = dropDownItems.GetEnumerator())
    while (dropDownCollectionEnumerator.MoveNext())
        Console.WriteLine(dropDownCollectionEnumerator.Current);

// هناك طريقتان لإزالة العناصر من مجموعة العناصر المنسدلة.
// 1 - إزالة عنصر بمحتويات مساوية للسلسلة التي تم تمريرها:
dropDownItems.Remove("Four");

// 2 - إزالة عنصر من الفهرس:
dropDownItems.RemoveAt(3);

Assert.AreEqual(3, dropDownItems.Count);
Assert.IsFalse(dropDownItems.Contains("Three and a half"));
Assert.IsFalse(dropDownItems.Contains("Four"));

doc.Save(ArtifactsDir + "FormFields.DropDownItemCollection.html");

// إفراغ المجموعة الكاملة من العناصر المنسدلة.
dropDownItems.Clear();
```

### أنظر أيضا

* class [FormField](../formfield/)
* property [DropDownItems](../formfield/dropdownitems/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)


