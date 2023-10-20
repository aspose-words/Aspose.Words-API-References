---
title: NodeCollection.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words لـ .NET
description: NodeCollection Clear طريقة. إزالة كافة العقد من هذه المجموعة ومن المستند في C#.
type: docs
weight: 40
url: /ar/net/aspose.words/nodecollection/clear/
---
## NodeCollection.Clear method

إزالة كافة العقد من هذه المجموعة ومن المستند.

```csharp
public void Clear()
```

## أمثلة

يوضح كيفية إزالة جميع الأقسام من المستند.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// يحتوي هذا المستند على قسم واحد به عدد قليل من العقد الفرعية التي تحتوي على جميع محتويات المستند وتعرضها.
Assert.AreEqual(1, doc.Sections.Count);
Assert.AreEqual(17, doc.Sections[0].GetChildNodes(NodeType.Any, true).Count);
Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());

// امسح مجموعة الأقسام، مما سيؤدي إلى إزالة كافة العناصر الفرعية للمستند.
doc.Sections.Clear();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Any, true).Count);
Assert.AreEqual(string.Empty, doc.GetText().Trim());
```

### أنظر أيضا

* class [NodeCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
