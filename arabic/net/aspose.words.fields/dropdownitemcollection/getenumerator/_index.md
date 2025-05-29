---
title: DropDownItemCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة DropDownItemCollection GetEnumerator لتكرار عناصر المجموعة بسهولة. حسّن كفاءة البرمجة لديك اليوم!
type: docs
weight: 60
url: /ar/net/aspose.words.fields/dropdownitemcollection/getenumerator/
---
## DropDownItemCollection.GetEnumerator method

يعيد كائن عداد يمكن استخدامه للتكرار على جميع العناصر في المجموعة.

```csharp
public IEnumerator<string> GetEnumerator()
```

## أمثلة

يوضح كيفية إدراج حقل مربع المجموعة، وتحرير العناصر الموجودة في مجموعة العناصر الخاصة به.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإدراج مربع مجموعة، ثم تحقق من مجموعة عناصر القائمة المنسدلة الخاصة به.
// في Microsoft Word، سيقوم المستخدم بالنقر فوق المربع المنسدل،
// ثم اختر أحد عناصر النص في المجموعة لعرضها.
string[] items = { "One", "Two", "Three" };
FormField comboBoxField = builder.InsertComboBox("DropDown", items, 0);
DropDownItemCollection dropDownItems = comboBoxField.DropDownItems;

Assert.AreEqual(3, dropDownItems.Count);
Assert.AreEqual("One", dropDownItems[0]);
Assert.AreEqual(1, dropDownItems.IndexOf("Two"));
Assert.IsTrue(dropDownItems.Contains("Three"));

// هناك طريقتان لإضافة عنصر جديد إلى مجموعة موجودة من عناصر القائمة المنسدلة.
// 1 - إضافة عنصر إلى نهاية المجموعة:
dropDownItems.Add("Four");

// 2 - إدراج عنصر قبل عنصر آخر في فهرس محدد:
dropDownItems.Insert(3, "Three and a half");

Assert.AreEqual(5, dropDownItems.Count);

// قم بالتكرار على المجموعة وطباعة كل عنصر.
using (IEnumerator<string> dropDownCollectionEnumerator = dropDownItems.GetEnumerator())
    while (dropDownCollectionEnumerator.MoveNext())
        Console.WriteLine(dropDownCollectionEnumerator.Current);

// هناك طريقتان لإزالة العناصر من مجموعة العناصر المنسدلة.
// 1 - إزالة عنصر يحتوي على محتويات مساوية للسلسلة المرسلة:
dropDownItems.Remove("Four");

// 2 - إزالة عنصر في الفهرس:
dropDownItems.RemoveAt(3);

Assert.AreEqual(3, dropDownItems.Count);
Assert.IsFalse(dropDownItems.Contains("Three and a half"));
Assert.IsFalse(dropDownItems.Contains("Four"));

doc.Save(ArtifactsDir + "FormFields.DropDownItemCollection.html");

//إفراغ المجموعة بأكملها من العناصر المنسدلة.
dropDownItems.Clear();
```

### أنظر أيضا

* class [DropDownItemCollection](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
