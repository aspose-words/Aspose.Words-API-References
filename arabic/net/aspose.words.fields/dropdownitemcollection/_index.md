---
title: DropDownItemCollection Class
linktitle: DropDownItemCollection
articleTitle: DropDownItemCollection
second_title: Aspose.Words لـ .NET
description: استكشف فئة Aspose.Words.Fields.DropDownItemCollection—الحل الأمثل لإدارة عناصر القائمة المنسدلة في حقول النماذج بسهولة!
type: docs
weight: 1910
url: /ar/net/aspose.words.fields/dropdownitemcollection/
---
## DropDownItemCollection class

مجموعة من السلاسل التي تمثل جميع العناصر في حقل نموذج القائمة المنسدلة.

لمعرفة المزيد، قم بزيارة[العمل مع الحقول](https://docs.aspose.com/words/net/working-with-fields/) مقالة توثيقية.

```csharp
public class DropDownItemCollection : IEnumerable<string>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words.fields/dropdownitemcollection/count/) { get; } | يحصل على عدد العناصر الموجودة في المجموعة. |
| [Item](../../aspose.words.fields/dropdownitemcollection/item/) { get; set; } | يحصل على العنصر أو يعينه عند الفهرس المحدد. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words.fields/dropdownitemcollection/add/)(*string*) | يضيف سلسلة إلى نهاية المجموعة. |
| [Clear](../../aspose.words.fields/dropdownitemcollection/clear/)() | يزيل جميع العناصر من المجموعة. |
| [Contains](../../aspose.words.fields/dropdownitemcollection/contains/)(*string*) | يحدد ما إذا كانت المجموعة تحتوي على القيمة المحددة. |
| [GetEnumerator](../../aspose.words.fields/dropdownitemcollection/getenumerator/)() | يعيد كائن عداد يمكن استخدامه للتكرار على جميع العناصر في المجموعة. |
| [IndexOf](../../aspose.words.fields/dropdownitemcollection/indexof/)(*string*) | يعيد الفهرس المبني على الصفر للقيمة المحددة في المجموعة. |
| [Insert](../../aspose.words.fields/dropdownitemcollection/insert/)(*int, string*) | يقوم بإدراج سلسلة في المجموعة عند الفهرس المحدد. |
| [Remove](../../aspose.words.fields/dropdownitemcollection/remove/)(*string*) | يزيل القيمة المحددة من المجموعة. |
| [RemoveAt](../../aspose.words.fields/dropdownitemcollection/removeat/)(*int*) | يزيل قيمة عند الفهرس المحدد. |

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

* class [FormField](../formfield/)
* property [DropDownItems](../formfield/dropdownitems/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)
