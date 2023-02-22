---
title: Document.AttachedTemplate
second_title: Referencia de API de Aspose.Words para .NET
description: Document propiedad. Obtiene o establece la ruta completa de la plantilla adjunta al documento.
type: docs
weight: 20
url: /es/net/aspose.words/document/attachedtemplate/
---
## Document.AttachedTemplate property

Obtiene o establece la ruta completa de la plantilla adjunta al documento.

```csharp
public string AttachedTemplate { get; set; }
```

### Excepciones

| excepción | condición |
| --- | --- |
| ArgumentNullException | Se lanza si intenta establecer un valor nulo. |

### Observaciones

Cadena vacía significa que el documento está adjunto a la plantilla Normal.

### Ejemplos

Muestra cómo configurar una plantilla predeterminada para documentos que no tienen plantillas adjuntas.

```csharp
Document doc = new Document();

// Habilite la actualización automática de estilo, pero no adjunte un documento de plantilla.
doc.AutomaticallyUpdateStyles = true;

Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// Dado que no hay un documento de plantilla, el documento no tenía dónde rastrear los cambios de estilo.
// Usar un objeto SaveOptions para configurar automáticamente una plantilla
// si un documento que estamos guardando no lo tiene.
SaveOptions options = SaveOptions.CreateSaveOptions("Document.DefaultTemplate.docx");
options.DefaultTemplate = MyDir + "Business brochure.dotx";

doc.Save(ArtifactsDir + "Document.DefaultTemplate.docx", options);
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../document/)
* asamblea [Aspose.Words](../../../)


