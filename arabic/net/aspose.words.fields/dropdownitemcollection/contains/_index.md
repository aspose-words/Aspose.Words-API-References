---
title: DropDownItemCollection.Contains
linktitle: Contains
articleTitle: Contains
second_title: Aspose.Words لـ .NET
description: DropDownItemCollection Contains طريقة. تحديد ما إذا كانت المجموعة تحتوي على القيمة المحددة في C#.
type: docs
weight: 50
url: /ar/net/aspose.words.fields/dropdownitemcollection/contains/
---
## DropDownItemCollection.Contains method

تحديد ما إذا كانت المجموعة تحتوي على القيمة المحددة.

```csharp
public bool Contains(string value)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| value | String | قيمة حساسة لحالة الأحرف لتحديد موقعها. |

### قيمة الإرجاع

`حقيقي` إذا تم العثور على العنصر في المجموعة؛ خلاف ذلك،`خطأ شنيع`.

## أمثلة

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
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
