---
title: Document.AutomaticallyUpdateStyles
second_title: Referencia de API de Aspose.Words para .NET
description: Document propiedad. Obtiene o establece un indicador que indica si los estilos del documento se actualizan para coincidir con los estilos de la plantilla adjunta cada vez que se abre el documento en MS Word.
type: docs
weight: 30
url: /es/net/aspose.words/document/automaticallyupdatestyles/
---
## Document.AutomaticallyUpdateStyles property

Obtiene o establece un indicador que indica si los estilos del documento se actualizan para coincidir con los estilos de la plantilla adjunta cada vez que se abre el documento en MS Word.

```csharp
public bool AutomaticallyUpdateStyles { get; set; }
```

### Ejemplos

Muestra cómo adjuntar una plantilla a un documento.

```csharp
Document doc = new Document();

// Los documentos de Microsoft Word por defecto vienen con una plantilla adjunta llamada "Normal.dotm".
// No existe una plantilla predeterminada para los documentos en blanco de Aspose.Words.
Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// Adjunte una plantilla, luego configure la bandera para aplicar cambios de estilo
// dentro de la plantilla a estilos en nuestro documento.
doc.AttachedTemplate = MyDir + "Business brochure.dotx";
doc.AutomaticallyUpdateStyles = true;

doc.Save(ArtifactsDir + "Document.AutomaticallyUpdateStyles.docx");
```

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


