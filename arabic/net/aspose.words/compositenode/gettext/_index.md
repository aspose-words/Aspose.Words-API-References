---
title: CompositeNode.GetText
second_title: Aspose.Words لمراجع .NET API
description: CompositeNode طريقة. الحصول على نص هذه العقدة وجميع أبنائها.
type: docs
weight: 130
url: /ar/net/aspose.words/compositenode/gettext/
---
## CompositeNode.GetText method

الحصول على نص هذه العقدة وجميع أبنائها.

```csharp
public override string GetText()
```

### ملاحظات

تتضمن السلسلة التي تم إرجاعها جميع عناصر التحكم والأحرف الخاصة كما هو موضح في[`ControlChar`](../../controlchar/).

### أمثلة

يُظهر الفرق بين استدعاء طريقتي GetText وToString على العقدة.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField("MERGEFIELD Field");

// سيقوم GetText باسترداد النص المرئي بالإضافة إلى رموز الحقول والأحرف الخاصة.
Assert.AreEqual("\u0013MERGEFIELD Field\u0014«Field»\u0015\u000c", doc.GetText());

// ToString سيعطينا مظهر المستند إذا تم حفظه بتنسيق حفظ تم تمريره.
Assert.AreEqual("«Field»\r\n", doc.ToString(SaveFormat.Text));
```

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

* class [CompositeNode](../)
* مساحة الاسم [Aspose.Words](../../compositenode/)
* المجسم [Aspose.Words](../../../)


