---
title: Node.PreviousSibling
linktitle: PreviousSibling
articleTitle: PreviousSibling
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Node PreviousSibling للوصول بسهولة إلى العقدة التي تأتي قبل العقدة الحالية لديك، مما يعزز مهاراتك في التعامل مع DOM.
type: docs
weight: 70
url: /ar/net/aspose.words/node/previoussibling/
---
## Node.PreviousSibling property

يحصل على العقدة التي تسبق هذه العقدة مباشرةً.

```csharp
public Node PreviousSibling { get; }
```

## ملاحظات

إذا لم تكن هناك عقدة سابقة،`باطل` تم إرجاعه.

## أمثلة

يوضح كيفية استخدام طرق Node و CompositeNode لإزالة قسم قبل القسم الأخير في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1 text.");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Writeln("Section 2 text.");

// كلا القسمين شقيقان لبعضهما البعض.
Section lastSection = (Section)doc.LastChild;
Section firstSection = (Section)lastSection.PreviousSibling;

// قم بإزالة قسم بناءً على علاقته الشقيقة بقسم آخر.
if (lastSection.PreviousSibling != null)
    doc.RemoveChild(firstSection);

// القسم الذي قمنا بإزالته هو القسم الأول، ولم يتبق للمستند سوى القسم الثاني.
Assert.AreEqual("Section 2 text.", doc.GetText().Trim());
```

### أنظر أيضا

* class [Node](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
