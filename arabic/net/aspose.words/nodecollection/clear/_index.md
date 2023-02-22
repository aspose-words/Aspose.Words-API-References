---
title: NodeCollection.Clear
second_title: Aspose.Words لمراجع .NET API
description: NodeCollection طريقة. يزيل كافة العقد من هذه المجموعة ومن المستند.
type: docs
weight: 40
url: /ar/net/aspose.words/nodecollection/clear/
---
## NodeCollection.Clear method

يزيل كافة العقد من هذه المجموعة ومن المستند.

```csharp
public void Clear()
```

### أمثلة

يوضح كيفية إزالة كافة الأقسام من المستند.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// يحتوي هذا المستند على قسم واحد به عدد قليل من العقد الفرعية التي تحتوي على جميع محتويات المستند وتعرضها.
Assert.AreEqual(1, doc.Sections.Count);
Assert.AreEqual(17, doc.Sections[0].GetChildNodes(NodeType.Any, true).Count);
Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());

// امسح مجموعة الأقسام ، والتي ستزيل جميع توابع المستند.
doc.Sections.Clear();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Any, true).Count);
Assert.AreEqual(string.Empty, doc.GetText().Trim());
```

### أنظر أيضا

* class [NodeCollection](../)
* مساحة الاسم [Aspose.Words](../../nodecollection/)
* المجسم [Aspose.Words](../../../)


