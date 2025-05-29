---
title: CompositeNode.GetText
linktitle: GetText
articleTitle: GetText
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة CompositeNode GetText لاسترداد النص بكفاءة من العقد وأبنائها، مما يعزز قدرات معالجة البيانات لديك.
type: docs
weight: 130
url: /ar/net/aspose.words/compositenode/gettext/
---
## CompositeNode.GetText method

يحصل على نص هذه العقدة وجميع أبنائها.

```csharp
public override string GetText()
```

## ملاحظات

تتضمن السلسلة المرتجعة جميع أحرف التحكم والأحرف الخاصة كما هو موضح في[`ControlChar`](../../controlchar/).

## أمثلة

يُظهر الفرق بين استدعاء طريقتي GetText وToString على عقدة.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField("MERGEFIELD Field");

// سيقوم GetText باسترجاع النص المرئي بالإضافة إلى رموز الحقول والأحرف الخاصة.
Assert.AreEqual("\u0013MERGEFIELD Field\u0014«Field»\u0015", doc.GetText().Trim());

// سيعطينا ToString مظهر المستند إذا تم حفظه بتنسيق الحفظ الذي تم تمريره.
Assert.AreEqual("«Field»", doc.ToString(SaveFormat.Text).Trim());
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

* class [CompositeNode](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
