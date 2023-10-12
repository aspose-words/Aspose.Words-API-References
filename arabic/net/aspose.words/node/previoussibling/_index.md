---
title: Node.PreviousSibling
second_title: Aspose.Words لمراجع .NET API
description: Node ملكية. يحصل على العقدة التي تسبق هذه العقدة مباشرة.
type: docs
weight: 70
url: /ar/net/aspose.words/node/previoussibling/
---
## Node.PreviousSibling property

يحصل على العقدة التي تسبق هذه العقدة مباشرة.

```csharp
public Node PreviousSibling { get; }
```

### ملاحظات

إذا لم تكن هناك عقدة سابقة، أ`باطل` تم إرجاعها.

### أمثلة

يوضح كيفية استخدام طريقتي Node وCompositeNode لإزالة قسم قبل القسم الأخير في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1 text.");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Writeln("Section 2 text.");

// كلا القسمين أشقاء لبعضهما البعض.
Section lastSection = (Section)doc.LastChild;
Section firstSection = (Section)lastSection.PreviousSibling;

// إزالة قسم بناءً على علاقة الأخوة مع قسم آخر.
if (lastSection.PreviousSibling != null)
    doc.RemoveChild(firstSection);

// القسم الذي أزلناه هو الأول، وتركنا الوثيقة مع الثاني فقط.
Assert.AreEqual("Section 2 text.", doc.GetText().Trim());
```

### أنظر أيضا

* class [Node](../)
* مساحة الاسم [Aspose.Words](../../node/)
* المجسم [Aspose.Words](../../../)


