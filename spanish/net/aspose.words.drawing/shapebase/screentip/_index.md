---
title: ShapeBase.ScreenTip
second_title: Referencia de API de Aspose.Words para .NET
description: ShapeBase propiedad. Define el texto que se muestra cuando el puntero del mouse se mueve sobre la forma.
type: docs
weight: 440
url: /es/net/aspose.words.drawing/shapebase/screentip/
---
## ShapeBase.ScreenTip property

Define el texto que se muestra cuando el puntero del mouse se mueve sobre la forma.

```csharp
public string ScreenTip { get; set; }
```

### Observaciones

El valor predeterminado es una cadena vacía.

### Ejemplos

Muestra cómo insertar una forma que contiene una imagen y también es un hipervínculo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.HRef = "https://foro.aspose.com/";
shape.Target = "New Window";
shape.ScreenTip = "Aspose.Words Support Forums";

// Ctrl + clic izquierdo en la forma en Microsoft Word abrirá una nueva ventana del navegador web
// y nos lleva al hipervínculo en la propiedad "HRef".
doc.Save(ArtifactsDir + "Image.InsertImageWithHyperlink.docx");
```

### Ver también

* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../shapebase/)
* asamblea [Aspose.Words](../../../)


