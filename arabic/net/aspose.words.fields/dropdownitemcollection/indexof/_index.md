---
title: DropDownItemCollection.IndexOf
second_title: Aspose.Words لمراجع .NET API
description: DropDownItemCollection طريقة. إرجاع الفهرس الصفري للقيمة المحددة في المجموعة.
type: docs
weight: 70
url: /ar/net/aspose.words.fields/dropdownitemcollection/indexof/
---
## DropDownItemCollection.IndexOf method

إرجاع الفهرس الصفري للقيمة المحددة في المجموعة.

```csharp
public int IndexOf(string value)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| value | String | القيمة الحساسة لحالة الأحرف المطلوب تحديد موقعها. |

### قيمة الإرجاع

المؤشر القائم على الصفر. قيمة سلبية إذا لم يتم العثور عليها.

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

* class [DropDownItemCollection](../)
* مساحة الاسم [Aspose.Words.Fields](../../dropdownitemcollection/)
* المجسم [Aspose.Words](../../../)


