---
title: SubDocument.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية SubDocument NodeType التي تقوم بإرجاع بيانات SubDocument بكفاءة، مما يعمل على تحسين قدرات إدارة المستندات ومعالجتها.
type: docs
weight: 10
url: /ar/net/aspose.words/subdocument/nodetype/
---
## SubDocument.NodeType property

إرجاعSubDocument .

```csharp
public override NodeType NodeType { get; }
```

## أمثلة

يوضح كيفية الوصول إلى المستند الفرعي للمستند الرئيسي.

```csharp
Document doc = new Document(MyDir + "Master document.docx");

NodeCollection subDocuments = doc.GetChildNodes(NodeType.SubDocument, true);
// تعمل هذه العقدة كمرجع لمستند خارجي، ولا يمكن الوصول إلى محتوياته.
SubDocument subDocument = (SubDocument)subDocuments[0];

Assert.False(subDocument.IsComposite);
```

### أنظر أيضا

* enum [NodeType](../../nodetype/)
* class [SubDocument](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
