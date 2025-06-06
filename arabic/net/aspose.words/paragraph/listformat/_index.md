---
title: Paragraph.ListFormat
linktitle: ListFormat
articleTitle: ListFormat
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Paragraph ListFormat للوصول بسهولة إلى تنسيق قائمة فقراتك وتخصيصها، مما يعزز عرض مستندك.
type: docs
weight: 150
url: /ar/net/aspose.words/paragraph/listformat/
---
## Paragraph.ListFormat property

يوفر الوصول إلى خصائص تنسيق القائمة للفقرة.

```csharp
public ListFormat ListFormat { get; }
```

## أمثلة

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

* class [ListFormat](../../../aspose.words.lists/listformat/)
* class [Paragraph](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
