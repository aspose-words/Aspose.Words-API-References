---
title: OleFormat.GetRawData
linktitle: GetRawData
articleTitle: GetRawData
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة GetRawData الخاصة بـ OleFormat لاسترداد البيانات الخام الخاصة بكائنات OLE بسهولة، مما يعزز قدراتك على إدارة البيانات وتكاملها.
type: docs
weight: 150
url: /ar/net/aspose.words.drawing/oleformat/getrawdata/
---
## OleFormat.GetRawData method

يحصل على بيانات خام لكائن OLE.

```csharp
public byte[] GetRawData()
```

## أمثلة

يوضح كيفية الوصول إلى البيانات الخام لكائن OLE المضمن.

```csharp
Document doc = new Document(MyDir + "OLE objects.docx");

foreach (Shape shape in doc.GetChildNodes(NodeType.Shape, true))
{
    OleFormat oleFormat = shape.OleFormat;
    if (oleFormat != null)
    {
        Console.WriteLine($"This is {(oleFormat.IsLink ? "a linked" : "an embedded")} object");
        byte[] oleRawData = oleFormat.GetRawData();

        Assert.AreEqual(24576, oleRawData.Length);
    }
}
```

### أنظر أيضا

* class [OleFormat](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
