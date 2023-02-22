---
title: ShapeBase.MarkupLanguage
second_title: Aspose.Words لمراجع .NET API
description: ShapeBase ملكية. Gets MarkupLanguage المستخدمة لهذا الكائن الرسومي.
type: docs
weight: 370
url: /ar/net/aspose.words.drawing/shapebase/markuplanguage/
---
## ShapeBase.MarkupLanguage property

Gets MarkupLanguage المستخدمة لهذا الكائن الرسومي.

```csharp
public ShapeMarkupLanguage MarkupLanguage { get; }
```

### أمثلة

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
* مساحة الاسم [Aspose.Words.Drawing](../../shapebase/)
* المجسم [Aspose.Words](../../../)


