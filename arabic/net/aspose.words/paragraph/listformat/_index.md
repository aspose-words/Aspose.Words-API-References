---
title: Paragraph.ListFormat
second_title: Aspose.Words لمراجع .NET API
description: Paragraph ملكية. يوفر الوصول إلى خصائص تنسيق القائمة الخاصة بالفقرة.
type: docs
weight: 150
url: /ar/net/aspose.words/paragraph/listformat/
---
## Paragraph.ListFormat property

يوفر الوصول إلى خصائص تنسيق القائمة الخاصة بالفقرة.

```csharp
public ListFormat ListFormat { get; }
```

### أمثلة

يوضح كيفية إخراج كافة الفقرات في مستند عبارة عن عناصر قائمة.

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

* class [ListFormat](../../../aspose.words.lists/listformat/)
* class [Paragraph](../)
* مساحة الاسم [Aspose.Words](../../paragraph/)
* المجسم [Aspose.Words](../../../)


