---
title: ListCollection.GetListByListId
linktitle: GetListByListId
articleTitle: GetListByListId
second_title: Aspose.Words لـ .NET
description: احصل على قائمتك المطلوبة بسهولة باستخدام طريقة GetListByListId. تمتع بالوصول السريع إلى البيانات باستخدام مُعرّف قائمة بسيط لتحسين الكفاءة.
type: docs
weight: 80
url: /ar/net/aspose.words.lists/listcollection/getlistbylistid/
---
## ListCollection.GetListByListId method

يحصل على قائمة من خلال معرف القائمة.

```csharp
public List GetListByListId(int listId)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| listId | Int32 | معرف القائمة. |

### قيمة الإرجاع

إرجاع كائن القائمة. إرجاع`باطل` إذا لم يتم العثور على قائمة بالمعرف المحدد.

## ملاحظات

لا تحتاج عادةً إلى استخدام هذه الطريقة. في أغلب الأحيان، تُطبّق list formatting على الفقرات بمجرد ضبط[`List`](../../listformat/list/) property من[`ListFormat`](../../listformat/) هدف.

## أمثلة

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
* مساحة الاسم [Aspose.Words.Lists](../../../aspose.words.lists/)
* المجسم [Aspose.Words](../../../)
