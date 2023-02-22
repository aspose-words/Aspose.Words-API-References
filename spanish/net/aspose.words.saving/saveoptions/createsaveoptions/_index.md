---
title: SaveOptions.CreateSaveOptions
second_title: Referencia de API de Aspose.Words para .NET
description: SaveOptions método. Crea un objeto de opciones de guardado de una clase adecuada para el formato de guardado especificado.
type: docs
weight: 10
url: /es/net/aspose.words.saving/saveoptions/createsaveoptions/
---
## CreateSaveOptions(SaveFormat) {#createsaveoptions}

Crea un objeto de opciones de guardado de una clase adecuada para el formato de guardado especificado.

```csharp
public static SaveOptions CreateSaveOptions(SaveFormat saveFormat)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| saveFormat | SaveFormat | El formato de guardado para el que se va a crear un objeto de opciones de guardado. |

### Valor_devuelto

Un objeto de una clase que se deriva de[`SaveOptions`](../).

### Ejemplos

Muestra una opción para optimizar el consumo de memoria al renderizar documentos grandes a PDF.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);

// Establezca la propiedad "MemoryOptimization" en "true" para reducir la huella de memoria de las operaciones de guardado de documentos grandes
// a costa de aumentar la duración de la operación.
// Establezca la propiedad "MemoryOptimization" en "false" para guardar el documento como PDF normalmente.
saveOptions.MemoryOptimization = memoryOptimization;

doc.Save(ArtifactsDir + "PdfSaveOptions.MemoryOptimization.pdf", saveOptions);
```

### Ver también

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../saveoptions/)
* asamblea [Aspose.Words](../../../)

---

## CreateSaveOptions(string) {#createsaveoptions_1}

Crea un objeto de opciones de guardado de una clase adecuada para la extensión de archivo especificada en el nombre de archivo proporcionado.

```csharp
public static SaveOptions CreateSaveOptions(string fileName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fileName | String | La extensión de este nombre de archivo determina la clase del objeto de opciones de guardado que se va a crear. |

### Valor_devuelto

Un objeto de una clase que se deriva de[`SaveOptions`](../).

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

* class [SaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../saveoptions/)
* asamblea [Aspose.Words](../../../)


