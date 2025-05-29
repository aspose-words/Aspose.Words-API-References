---
title: Document.AttachedTemplate
linktitle: AttachedTemplate
articleTitle: AttachedTemplate
second_title: Aspose.Words para .NET
description: Descubra cómo administrar eficientemente su propiedad Document AttachedTemplate. Configure o recupere fácilmente la ruta completa de la plantilla de su documento para una integración perfecta.
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
| ArgumentNullException | Se lanza si intenta establecer en un`nulo` valor. |

## Observaciones

Una cadena vacía significa que el documento está adjunto a la plantilla Normal.

## Ejemplos

Muestra cómo establecer una plantilla predeterminada para documentos que no tienen plantillas adjuntas.

```csharp
Document doc = new Document();

// Habilite la actualización automática de estilos, pero no adjunte un documento de plantilla.
doc.AutomaticallyUpdateStyles = true;

Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// Como no existe un documento de plantilla, el documento no tenía dónde rastrear los cambios de estilo.
// Utilice un objeto SaveOptions para establecer automáticamente una plantilla
// si un documento que estamos guardando no tiene uno.
SaveOptions options = SaveOptions.CreateSaveOptions("Document.DefaultTemplate.docx");
options.DefaultTemplate = MyDir + "Business brochure.dotx";

doc.Save(ArtifactsDir + "Document.DefaultTemplate.docx", options);
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
