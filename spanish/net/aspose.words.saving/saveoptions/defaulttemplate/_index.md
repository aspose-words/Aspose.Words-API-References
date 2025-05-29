---
title: SaveOptions.DefaultTemplate
linktitle: DefaultTemplate
articleTitle: DefaultTemplate
second_title: Aspose.Words para .NET
description: ¡Administre sus opciones de guardado fácilmente! Configure u obtenga la ruta y el nombre de archivo predeterminados de la plantilla para optimizar el procesamiento de documentos. ¡Optimice su flujo de trabajo hoy mismo!
type: docs
weight: 40
url: /es/net/aspose.words.saving/saveoptions/defaulttemplate/
---
## SaveOptions.DefaultTemplate property

Obtiene o establece la ruta a la plantilla predeterminada (incluido el nombre del archivo). El valor predeterminado para esta propiedad es**cadena vacía** (Empty ).

```csharp
public string DefaultTemplate { get; set; }
```

## Observaciones

Si se especifica, esta ruta se utiliza para cargar la plantilla cuando[`AutomaticallyUpdateStyles`](../../../aspose.words/document/automaticallyupdatestyles/) es`verdadero` , pero[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) Está vacío.

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

* class [SaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
