---
title: ShapeBase.MarkupLanguage
linktitle: MarkupLanguage
articleTitle: MarkupLanguage
second_title: Aspose.Words لـ .NET
description: ShapeBase MarkupLanguage ملكية. يحصل على لغة الترميز المستخدمة لهذا الكائن الرسومي في C#.
type: docs
weight: 390
url: /ar/net/aspose.words.drawing/shapebase/markuplanguage/
---
## ShapeBase.MarkupLanguage property

يحصل على لغة الترميز المستخدمة لهذا الكائن الرسومي.

```csharp
public ShapeMarkupLanguage MarkupLanguage { get; }
```

## أمثلة

يوضح كيفية التحقق من حجم الشكل ولغة الترميز.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Dml, shape.MarkupLanguage);
Assert.AreEqual(new SizeF(300, 300), shape.SizeInPoints);
```

### أنظر أيضا

* enum [ShapeMarkupLanguage](../../shapemarkuplanguage/)
* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
