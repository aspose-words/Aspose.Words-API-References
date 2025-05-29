---
title: ShapeBase.ScreenTip
linktitle: ScreenTip
articleTitle: ScreenTip
second_title: Aspose.Words para .NET
description: Descubra la propiedad ShapeBase ScreenTip, mejore la experiencia del usuario personalizando el texto de información sobre herramientas que aparece cuando pasa el mouse sobre las formas.
type: docs
weight: 510
url: /es/net/aspose.words.drawing/shapebase/screentip/
---
## ShapeBase.ScreenTip property

Define el texto que se muestra cuando el puntero del mouse se mueve sobre la forma.

```csharp
public string ScreenTip { get; set; }
```

## Observaciones

El valor predeterminado es una cadena vacía.

## Ejemplos

Muestra cómo insertar una forma que contiene una imagen y también es un hipervínculo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.HRef = "https://forum.aspose.com/";
shape.Target = "New Window";
shape.ScreenTip = "Aspose.Words Support Forums";

// Al presionar Ctrl + clic izquierdo en la forma en Microsoft Word se abrirá una nueva ventana del navegador web
// y nos lleva al hipervínculo en la propiedad "HRef".
doc.Save(ArtifactsDir + "Image.InsertImageWithHyperlink.docx");
```

### Ver también

* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
