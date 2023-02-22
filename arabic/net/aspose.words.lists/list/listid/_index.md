---
title: List.ListId
second_title: Aspose.Words لمراجع .NET API
description: List ملكية. الحصول على المعرف الفريد للقائمة .
type: docs
weight: 60
url: /ar/net/aspose.words.lists/list/listid/
---
## List.ListId property

الحصول على المعرف الفريد للقائمة .

```csharp
public int ListId { get; }
```

### ملاحظات

لا تحتاج عادة إلى استخدام هذه الخاصية. ولكن إذا كنت تستخدمه ، فأنت تفعل ذلك عادةً جنبًا إلى جنب مع ملف[`GetListByListId`](../../listcollection/getlistbylistid/) طريقة للعثور على قائمة a بواسطة معرفها.

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

يوضح كيفية إخراج كل الفقرات في مستند تكون من عناصر القائمة.

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

foreach (Paragraph para in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem))
{ 
    Console.WriteLine($"This paragraph belongs to list ID# {para.ListFormat.List.ListId}, number style \"{para.ListFormat.ListLevel.NumberStyle}\"");
    Console.WriteLine($"\t\"{para.GetText().Trim()}\"");
}
```

### أنظر أيضا

* class [List](../)
* مساحة الاسم [Aspose.Words.Lists](../../list/)
* المجسم [Aspose.Words](../../../)


