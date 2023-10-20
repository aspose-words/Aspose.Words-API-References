---
title: ViewOptions.FormsDesign
linktitle: FormsDesign
articleTitle: FormsDesign
second_title: Aspose.Words para .NET
description: ViewOptions FormsDesign propiedad. Especifica si el documento está en modo de diseño de formularios en C#.
type: docs
weight: 30
url: /es/net/aspose.words.settings/viewoptions/formsdesign/
---
## ViewOptions.FormsDesign property

Especifica si el documento está en modo de diseño de formularios.

```csharp
public bool FormsDesign { get; set; }
```

## Observaciones

Actualmente sólo funciona con documentos en formato WordML.

## Ejemplos

Muestra cómo habilitar/deshabilitar el modo de diseño de formularios.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Establece la propiedad "FormsDesign" en "false" para mantener el modo de diseño de formularios deshabilitado.
// Establece la propiedad "FormsDesign" en "true" para habilitar el modo de diseño de formularios.
doc.ViewOptions.FormsDesign = useFormsDesign;

doc.Save(ArtifactsDir + "ViewOptions.FormsDesign.xml");

Assert.AreEqual(useFormsDesign,
    File.ReadAllText(ArtifactsDir + "ViewOptions.FormsDesign.xml").Contains("<w:formsDesign />"));
```

### Ver también

* class [ViewOptions](../)
* espacio de nombres [Aspose.Words.Settings](../../../aspose.words.settings/)
* asamblea [Aspose.Words](../../../)
