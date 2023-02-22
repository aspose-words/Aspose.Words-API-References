---
title: ListCollection.GetListByListId
second_title: Aspose.Words لمراجع .NET API
description: ListCollection طريقة. الحصول على قائمة بواسطة معرف القائمة .
type: docs
weight: 70
url: /ar/net/aspose.words.lists/listcollection/getlistbylistid/
---
## ListCollection.GetListByListId method

الحصول على قائمة بواسطة معرف القائمة .

```csharp
public List GetListByListId(int listId)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| listId | Int32 | معرف القائمة. |

### قيمة الإرجاع

إرجاع كائن القائمة. إرجاع القيمة فارغة إذا لم يتم العثور على قائمة بالمعرف المحدد.

### ملاحظات

لا تحتاج عادةً إلى استخدام هذه الطريقة. في معظم الأوقات ، تقوم بتطبيق تنسيق القائمة على الفقرات فقط من خلال إعدادات ملف[`List`](../../listformat/list/) property من[`ListFormat`](../../listformat/) هدف.

### أمثلة

يوضح كيفية التحقق من خصائص مستند المالك للقوائم.

```csharp
Document doc = new Document();

ListCollection lists = doc.Lists;

Assert.AreEqual(doc, lists.Document);

List list = lists.Add(ListTemplate.BulletDefault);

Assert.AreEqual(doc, list.Document);

Console.WriteLine("Current list count: " + lists.Count);
Console.WriteLine("Is the first document list: " + (lists[0].Equals(list)));
Console.WriteLine("ListId: " + list.ListId);
Console.WriteLine("List is the same by ListId: " + (lists.GetListByListId(1).Equals(list)));
```

### أنظر أيضا

* class [List](../../list/)
* class [ListCollection](../)
* مساحة الاسم [Aspose.Words.Lists](../../listcollection/)
* المجسم [Aspose.Words](../../../)


