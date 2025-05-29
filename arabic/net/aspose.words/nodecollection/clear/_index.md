---
title: NodeCollection.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words لـ .NET
description: قم بمسح NodeCollection الخاص بك بسهولة باستخدام طريقة Clear الخاصة بنا، وإزالة جميع العقد من المجموعة والمستند للحصول على الأداء الأمثل.
type: docs
weight: 40
url: /ar/net/aspose.words/nodecollection/clear/
---
## NodeCollection.Clear method

يزيل جميع العقد من هذه المجموعة ومن المستند.

```csharp
public void Clear()
```

## أمثلة

يوضح كيفية إزالة كافة الأقسام من المستند.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// تحتوي هذه الوثيقة على قسم واحد مع عدد قليل من العقد الفرعية التي تحتوي على كافة محتويات الوثيقة وتعرضها.
Assert.AreEqual(1, doc.Sections.Count);
Assert.AreEqual(17, doc.Sections[0].GetChildNodes(NodeType.Any, true).Count);
Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());

// قم بمسح مجموعة الأقسام، مما سيؤدي إلى إزالة جميع أقسام المستند.
doc.Sections.Clear();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Any, true).Count);
Assert.AreEqual(string.Empty, doc.GetText().Trim());
```

### أنظر أيضا

* class [NodeCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
