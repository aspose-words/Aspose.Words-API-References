---
title: SaveOptions.CreateSaveOptions
linktitle: CreateSaveOptions
articleTitle: CreateSaveOptions
second_title: Aspose.Words para .NET
description: Descubra el método CreateSaveOptions para generar fácilmente opciones de guardado adaptadas a su formato preferido, mejorando la eficiencia de la gestión de sus documentos.
type: docs
weight: 10
url: /es/net/aspose.words.saving/saveoptions/createsaveoptions/
---
## CreateSaveOptions(*[SaveFormat](../../../aspose.words/saveformat/)*) {#createsaveoptions}

Crea un objeto de opciones de guardado de una clase adecuada para el formato de guardado especificado.

```csharp
public static SaveOptions CreateSaveOptions(SaveFormat saveFormat)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| saveFormat | SaveFormat | El formato de guardado para el cual se creará un objeto de opciones de guardado. |

### Valor_devuelto

Un objeto de una clase que deriva de[`SaveOptions`](../).

## Ejemplos

Muestra una opción para optimizar el consumo de memoria al convertir documentos grandes a PDF.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Crea un objeto "PdfSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .PDF.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);

// Establezca la propiedad "MemoryOptimization" en "verdadero" para reducir el consumo de memoria de las operaciones de guardado de documentos grandes
// a costa de aumentar la duración de la operación.
// Establezca la propiedad "MemoryOptimization" en "falso" para guardar el documento como PDF normalmente.
saveOptions.MemoryOptimization = memoryOptimization;

doc.Save(ArtifactsDir + "PdfSaveOptions.MemoryOptimization.pdf", saveOptions);
```

### Ver también

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)

---

## CreateSaveOptions(*string*) {#createsaveoptions_1}

Crea un objeto de opciones de guardado de una clase adecuada para la extensión de archivo especificada en el nombre de archivo dado.

```csharp
public static SaveOptions CreateSaveOptions(string fileName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fileName | String | La extensión de este nombre de archivo determina la clase del objeto de opciones de guardado a crear. |

### Valor_devuelto

Un objeto de una clase que deriva de[`SaveOptions`](../).

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
