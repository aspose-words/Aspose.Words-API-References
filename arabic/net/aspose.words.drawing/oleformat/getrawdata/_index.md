---
title: OleFormat.GetRawData
linktitle: GetRawData
articleTitle: GetRawData
second_title: Aspose.Words لـ .NET
description: OleFormat GetRawData طريقة. يحصل على البيانات الأولية لكائن OLE في C#.
type: docs
weight: 150
url: /ar/net/aspose.words.drawing/oleformat/getrawdata/
---
## OleFormat.GetRawData method

يحصل على البيانات الأولية لكائن OLE.

```csharp
public byte[] GetRawData()
```

## أمثلة

يوضح كيفية الوصول إلى البيانات الأولية لكائن OLE المضمن.

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
