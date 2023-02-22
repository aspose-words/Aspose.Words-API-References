---
title: ViewOptions.FormsDesign
second_title: Referencia de API de Aspose.Words para .NET
description: ViewOptions propiedad. Especifica si el documento está en modo de diseño de formularios.
type: docs
weight: 30
url: /es/net/aspose.words.settings/viewoptions/formsdesign/
---
## ViewOptions.FormsDesign property

Especifica si el documento está en modo de diseño de formularios.

```csharp
public bool FormsDesign { get; set; }
```

### Observaciones

Actualmente solo funciona para documentos en formato WordML.

### Ejemplos

Muestra cómo habilitar/deshabilitar el modo de diseño de formularios.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Establezca la propiedad "FormsDesign" en "falso" para mantener el modo de diseño de formularios deshabilitado.
// Establezca la propiedad "FormsDesign" en "true" para habilitar el modo de diseño de formularios.
doc.ViewOptions.FormsDesign = useFormsDesign;

doc.Save(ArtifactsDir + "ViewOptions.FormsDesign.xml");

Assert.AreEqual(useFormsDesign,
    File.ReadAllText(ArtifactsDir + "ViewOptions.FormsDesign.xml").Contains("<w:formsDesign />"));
```

### Ver también

* class [ViewOptions](../)
* espacio de nombres [Aspose.Words.Settings](../../viewoptions/)
* asamblea [Aspose.Words](../../../)


