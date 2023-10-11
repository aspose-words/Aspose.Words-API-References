---
title: SubDocument.NodeType
second_title: Aspose.Words لمراجع .NET API
description: SubDocument ملكية. إرجاعSubDocument .
type: docs
weight: 10
url: /ar/net/aspose.words/subdocument/nodetype/
---
## SubDocument.NodeType property

إرجاعSubDocument .

```csharp
public override NodeType NodeType { get; }
```

### أمثلة

يوضح كيفية الوصول إلى المستند الثانوي للمستند الرئيسي.

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
* مساحة الاسم [Aspose.Words](../../subdocument/)
* المجسم [Aspose.Words](../../../)


