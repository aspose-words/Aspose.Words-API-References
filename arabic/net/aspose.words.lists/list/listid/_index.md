---
title: List.ListId
linktitle: ListId
articleTitle: ListId
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ListId الفريدة للوصول إلى قوائمك وإدارتها بسهولة. سهّل سير عملك باستخدام هذا المُعرِّف الأساسي.
type: docs
weight: 60
url: /ar/net/aspose.words.lists/list/listid/
---
## List.ListId property

يحصل على معرف فريد للقائمة.

```csharp
public int ListId { get; }
```

## ملاحظات

لا تحتاج عادةً إلى استخدام هذه الخاصية. ولكن إذا استخدمتها، فستفعل ذلك عادةً بالتزامن مع[`GetListByListId`](../../listcollection/getlistbylistid/) طريقة للعثور على قائمة a من خلال معرفها.

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

يوضح كيفية إخراج كافة الفقرات في المستند التي تعد عناصر قائمة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.ApplyNumberDefault();
builder.Writeln("Numbered list item 1");
builder.Writeln("Numbered list item 2");
builder.Writeln("Numbered list item 3");
builder.ListFormat.RemoveNumbers();

builder.ListFormat.ApplyBulletDefault();
builder.Writeln("Bulleted list item 1");
builder.Writeln("Bulleted list item 2");
builder.Writeln("Bulleted list item 3");
builder.ListFormat.RemoveNumbers();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

foreach (Paragraph para in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem).ToList())
{ 
    Console.WriteLine($"This paragraph belongs to list ID# {para.ListFormat.List.ListId}, number style \"{para.ListFormat.ListLevel.NumberStyle}\"");
    Console.WriteLine($"\t\"{para.GetText().Trim()}\"");
}
```

### أنظر أيضا

* class [List](../)
* مساحة الاسم [Aspose.Words.Lists](../../../aspose.words.lists/)
* المجسم [Aspose.Words](../../../)
