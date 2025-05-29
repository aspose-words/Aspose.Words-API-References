---
title: OleFormat.Clsid
linktitle: Clsid
articleTitle: Clsid
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية OleFormat Clsid لاسترداد CLSID الخاص بكائنات OLE بسهولة، مما يعزز وظائف تطبيقك وأدائه.
type: docs
weight: 20
url: /ar/net/aspose.words.drawing/oleformat/clsid/
---
## OleFormat.Clsid property

يحصل على CLSID لكائن OLE.

```csharp
public Guid Clsid { get; }
```

## أمثلة

يوضح كيفية الوصول إلى عنصر تحكم OLE المضمن في مستند وعناصر التحكم الفرعية الخاصة به.

```csharp
Document doc = new Document(MyDir + "OLE ActiveX controls.docm");

// تقوم الأشكال بتخزين وعرض كائنات OLE في نص المستند.
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual("6e182020-f460-11ce-9bcd-00aa00608e01", shape.OleFormat.Clsid.ToString());

Forms2OleControl oleControl = (Forms2OleControl)shape.OleFormat.OleControl;

// قد تحتوي بعض عناصر تحكم OLE على عناصر تحكم فرعية، مثل تلك الموجودة في هذه الوثيقة والتي تحتوي على ثلاثة أزرار خيارات.
Forms2OleControlCollection oleControlCollection = oleControl.ChildNodes;

Assert.AreEqual(3, oleControlCollection.Count);

Assert.AreEqual("C#", oleControlCollection[0].Caption);
Assert.AreEqual("1", oleControlCollection[0].Value);

Assert.AreEqual("Visual Basic", oleControlCollection[1].Caption);
Assert.AreEqual("0", oleControlCollection[1].Value);

Assert.AreEqual("Delphi", oleControlCollection[2].Caption);
Assert.AreEqual("0", oleControlCollection[2].Value);
```

### أنظر أيضا

* class [OleFormat](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
