---
title: ShapeBase.HRef
second_title: Referencia de API de Aspose.Words para .NET
description: ShapeBase propiedad. Obtiene o establece la dirección completa del hipervínculo para una forma.
type: docs
weight: 230
url: /es/net/aspose.words.drawing/shapebase/href/
---
## ShapeBase.HRef property

Obtiene o establece la dirección completa del hipervínculo para una forma.

```csharp
public string HRef { get; set; }
```

### Observaciones

El valor predeterminado es una cadena vacía.

A continuación se muestran ejemplos de valores válidos para esta propiedad:

URI completa:`https://www.aspose.com/`.

Nombre completo del archivo:`C:\\Mis documentos\\SalesReport.doc`.

URI relativa:`../../../recurso.txt`

Nombre de archivo relativo:`..\\Mis documentos\\SalesReport.doc`.

Marcar dentro de otro documento:`https://www.aspose.com/Products/Default.aspx#Suites`

Marcar dentro de este documento:`#NombreDeBookmak`.

### Ejemplos

Muestra cómo insertar una forma que contiene una imagen y también es un hipervínculo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.HRef = "https://forum.aspose.com/";
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


