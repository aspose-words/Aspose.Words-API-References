---
title: ShapeBase.MarkupLanguage
linktitle: MarkupLanguage
articleTitle: MarkupLanguage
second_title: Aspose.Words para .NET
description: Descubra la propiedad ShapeBase MarkupLanguage para una gestión optimizada de objetos gráficos. ¡Descubra hoy mismo una integración perfecta y una mayor eficiencia de diseño!
type: docs
weight: 410
url: /es/net/aspose.words.drawing/shapebase/markuplanguage/
---
## ShapeBase.MarkupLanguage property

Obtiene el lenguaje de marcado utilizado para este objeto gráfico.

```csharp
public ShapeMarkupLanguage MarkupLanguage { get; }
```

## Ejemplos

Muestra cómo verificar el tamaño de una forma y el lenguaje de marcado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Dml, shape.MarkupLanguage);
Assert.AreEqual(new SizeF(300, 300), shape.SizeInPoints);
```

### Ver también

* enum [ShapeMarkupLanguage](../../shapemarkuplanguage/)
* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
