---
title: ListCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ListCollection Count لاسترداد عدد القوائم المرقمة والمنقطة في مستندك بسهولة، مما يؤدي إلى تحسين تنظيم المحتوى لديك.
type: docs
weight: 10
url: /ar/net/aspose.words.lists/listcollection/count/
---
## ListCollection.Count property

يحصل على عدد القوائم المرقمة والمنقطة في المستند.

```csharp
public int Count { get; }
```

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

* class [ListCollection](../)
* مساحة الاسم [Aspose.Words.Lists](../../../aspose.words.lists/)
* المجسم [Aspose.Words](../../../)
