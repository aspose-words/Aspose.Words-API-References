---
title: ListCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words لـ .NET
description: ListCollection Item ملكية. الحصول على قائمة حسب الفهرس في C#.
type: docs
weight: 30
url: /ar/net/aspose.words.lists/listcollection/item/
---
## ListCollection indexer

الحصول على قائمة حسب الفهرس.

```csharp
public List this[int index] { get; }
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

يوضح كيفية تطبيق تنسيق القائمة لقائمة موجودة على مجموعة من الفقرات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1");
builder.Writeln("Paragraph 2");
builder.Write("Paragraph 3");

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

Assert.AreEqual(0, paras.Count(n => (n as Paragraph).ListFormat.IsListItem));

doc.Lists.Add(ListTemplate.NumberDefault);
List list = doc.Lists[0];

foreach (Paragraph paragraph in paras.OfType<Paragraph>())
{
    paragraph.ListFormat.List = list;
    paragraph.ListFormat.ListLevelNumber = 2;
}

Assert.AreEqual(3, paras.Count(n => (n as Paragraph).ListFormat.IsListItem));
```

### أنظر أيضا

* class [List](../../list/)
* class [ListCollection](../)
* مساحة الاسم [Aspose.Words.Lists](../../../aspose.words.lists/)
* المجسم [Aspose.Words](../../../)
