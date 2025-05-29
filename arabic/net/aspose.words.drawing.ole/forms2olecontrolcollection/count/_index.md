---
title: Forms2OleControlCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Count في Forms2OleControlCollection لاسترداد العدد الإجمالي للأشياء في مجموعتك بسهولة لتحسين إدارة البيانات.
type: docs
weight: 20
url: /ar/net/aspose.words.drawing.ole/forms2olecontrolcollection/count/
---
## Forms2OleControlCollection.Count property

يحصل على عدد الكائنات في المجموعة.

```csharp
public int Count { get; }
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

* class [Forms2OleControlCollection](../)
* مساحة الاسم [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* المجسم [Aspose.Words](../../../)
