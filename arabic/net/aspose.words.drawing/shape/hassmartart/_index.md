---
title: Shape.HasSmartArt
second_title: Aspose.Words لمراجع .NET API
description: Shape ملكية. إرجاعحقيقي اذا هذاShape يحتوي على كائن SmartArt.
type: docs
weight: 90
url: /ar/net/aspose.words.drawing/shape/hassmartart/
---
## Shape.HasSmartArt property

إرجاع`حقيقي` اذا هذا[`Shape`](../) يحتوي على كائن SmartArt.

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

* class [Shape](../)
* مساحة الاسم [Aspose.Words.Drawing](../../shape/)
* المجسم [Aspose.Words](../../../)


