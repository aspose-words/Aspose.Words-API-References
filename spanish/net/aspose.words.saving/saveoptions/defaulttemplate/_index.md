---
title: SaveOptions.DefaultTemplate
linktitle: DefaultTemplate
articleTitle: DefaultTemplate
second_title: Aspose.Words para .NET
description: SaveOptions DefaultTemplate propiedad. Obtiene o establece la ruta a la plantilla predeterminada incluido el nombre del archivo. El valor predeterminado para esta propiedad escuerda vacía Empty en C#.
type: docs
weight: 40
url: /es/net/aspose.words.saving/saveoptions/defaulttemplate/
---
## SaveOptions.DefaultTemplate property

Obtiene o establece la ruta a la plantilla predeterminada (incluido el nombre del archivo). El valor predeterminado para esta propiedad es**cuerda vacía** (Empty).

```csharp
public string DefaultTemplate { get; set; }
```

## Observaciones

Si se especifica, esta ruta se utiliza para cargar la plantilla cuando[`AutomaticallyUpdateStyles`](../../../aspose.words/document/automaticallyupdatestyles/) es`verdadero` , pero[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) esta vacio.

## Ejemplos

Muestra cómo configurar una plantilla predeterminada para documentos que no tienen plantillas adjuntas.

```csharp
Document doc = new Document();

// Habilite la actualización automática de estilo, pero no adjunte un documento de plantilla.
doc.AutomaticallyUpdateStyles = true;

Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// Como no hay un documento de plantilla, el documento no tenía ningún lugar para realizar un seguimiento de los cambios de estilo.
// Usa un objeto SaveOptions para configurar automáticamente una plantilla
// si un documento que estamos guardando no lo tiene.
SaveOptions options = SaveOptions.CreateSaveOptions("Document.DefaultTemplate.docx");
options.DefaultTemplate = MyDir + "Business brochure.dotx";

doc.Save(ArtifactsDir + "Document.DefaultTemplate.docx", options);
```

### Ver también

* class [SaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
