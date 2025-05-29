---
title: Document.AutomaticallyUpdateStyles
linktitle: AutomaticallyUpdateStyles
articleTitle: AutomaticallyUpdateStyles
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad AutomaticallyUpdateStyles en MS Word garantiza que los estilos de su documento se sincronicen con la plantilla cada vez que lo abre, mejorando la consistencia.
type: docs
weight: 30
url: /es/net/aspose.words/document/automaticallyupdatestyles/
---
## Document.AutomaticallyUpdateStyles property

Obtiene o establece un indicador que indica si los estilos del documento se actualizan para coincidir con los estilos de la plantilla adjunta cada vez que se abre el documento en MS Word.

```csharp
public bool AutomaticallyUpdateStyles { get; set; }
```

## Ejemplos

Muestra cómo adjuntar una plantilla a un documento.

```csharp
Document doc = new Document();

// Los documentos de Microsoft Word vienen por defecto con una plantilla adjunta llamada "Normal.dotm".
// No existe una plantilla predeterminada para documentos Aspose.Words en blanco.
Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// Adjunte una plantilla y luego configure la bandera para aplicar los cambios de estilo
// dentro de la plantilla a estilos en nuestro documento.
doc.AttachedTemplate = MyDir + "Business brochure.dotx";
doc.AutomaticallyUpdateStyles = true;

doc.Save(ArtifactsDir + "Document.AutomaticallyUpdateStyles.docx");
```

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
