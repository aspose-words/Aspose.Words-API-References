---
title: HasSmartArt
second_title: Aspose.Words لمراجع .NET API
description: إرجاع صحيح إذا كان هذا الشكل يحتوي على كائن SmartArt.
type: docs
weight: 90
url: /ar/net/aspose.words.drawing/shape/hassmartart/
---
## Shape.HasSmartArt property

إرجاع صحيح إذا كان هذا الشكل يحتوي على كائن SmartArt.

```csharp
public bool HasSmartArt { get; }
```

### أمثلة

يوضح كيفية حساب عدد الأشكال في مستند باستخدام كائنات SmartArt.

```csharp
Document doc = new Document(MyDir + "SmartArt.docx");

int numberOfSmartArtShapes = doc.GetChildNodes(NodeType.Shape, true).Cast<Shape>().Count(shape => shape.HasSmartArt);

Assert.AreEqual(2, numberOfSmartArtShapes);
```

### أنظر أيضا

* class [Shape](../../shape)
* مساحة الاسم [Aspose.Words.Drawing](../../shape)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
