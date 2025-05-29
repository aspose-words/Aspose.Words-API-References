---
title: ViewOptions.FormsDesign
linktitle: FormsDesign
articleTitle: FormsDesign
second_title: Aspose.Words para .NET
description: Descubra cómo ViewOptions FormsDesign mejora su experiencia con los documentos alternando el modo de diseño de formularios para una edición y personalización perfectas.
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

// Establezca la propiedad "FormsDesign" en "false" para mantener el modo de diseño de formularios deshabilitado.
// Establezca la propiedad "FormsDesign" en "verdadero" para habilitar el modo de diseño de formularios.
doc.ViewOptions.FormsDesign = useFormsDesign;

doc.Save(ArtifactsDir + "ViewOptions.FormsDesign.xml");

Assert.AreEqual(useFormsDesign,
    File.ReadAllText(ArtifactsDir + "ViewOptions.FormsDesign.xml").Contains("<w:formsDesign />"));
```

### Ver también

* class [ViewOptions](../)
* espacio de nombres [Aspose.Words.Settings](../../../aspose.words.settings/)
* asamblea [Aspose.Words](../../../)
