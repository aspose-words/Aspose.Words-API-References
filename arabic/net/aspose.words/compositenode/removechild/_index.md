---
title: CompositeNode.RemoveChild
linktitle: RemoveChild
articleTitle: RemoveChild
second_title: Aspose.Words لـ .NET
description: CompositeNode RemoveChild طريقة. إزالة العقدة الفرعية المحددة في C#.
type: docs
weight: 170
url: /ar/net/aspose.words/compositenode/removechild/
---
## CompositeNode.RemoveChild method

إزالة العقدة الفرعية المحددة.

```csharp
public Node RemoveChild(Node oldChild)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| oldChild | Node | العقدة المراد إزالتها. |

### قيمة الإرجاع

العقدة التي تمت إزالتها.

## ملاحظات

الوالد*oldChild* تم ضبطه على`باطل` بعد إزالة العقدة.

## أمثلة

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

* class [Node](../../node/)
* class [CompositeNode](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
