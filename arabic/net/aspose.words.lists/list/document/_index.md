---
title: List.Document
second_title: Aspose.Words لمراجع .NET API
description: List ملكية. الحصول على مستند المالك.
type: docs
weight: 10
url: /ar/net/aspose.words.lists/list/document/
---
## List.Document property

الحصول على مستند المالك.

```csharp
public DocumentBase Document { get; }
```

### ملاحظات

تحتوي القائمة دائمًا على مستند أصلي وتكون صالحة فقط في سياق هذا المستند.

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

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [List](../)
* مساحة الاسم [Aspose.Words.Lists](../../list/)
* المجسم [Aspose.Words](../../../)


