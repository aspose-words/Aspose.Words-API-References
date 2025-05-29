---
title: ShapeBase.HRef
linktitle: HRef
articleTitle: HRef
second_title: Aspose.Words para .NET
description: Descubra la propiedad ShapeBase HRef para administrar fácilmente direcciones de hipervínculos completas para sus formas, mejorando la interactividad y la funcionalidad de su diseño.
type: docs
weight: 250
url: /es/net/aspose.words.drawing/shapebase/href/
---
## ShapeBase.HRef property

Obtiene o establece la dirección de hipervínculo completa para una forma.

```csharp
public string HRef { get; set; }
```

## Observaciones

El valor predeterminado es una cadena vacía.

A continuación se muestran ejemplos de valores válidos para esta propiedad:

URI completa:`https://www.aspose.com/`.

Nombre completo del archivo:`C:\\Mis documentos\\Informe de ventas.doc`.

URI relativa:`../../../recurso.txt`

Nombre de archivo relativo:`..\\Mis documentos\\Informe de ventas.doc`.

Marcador dentro de otro documento:`https://www.aspose.com/Products/Default.aspx#Suites`

Marcador dentro de este documento:`#NombreDeLaMarcaDeLibro`.

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
