---
title: SaveOptions.UpdateSdtContent
second_title: Referencia de API de Aspose.Words para .NET
description: SaveOptions propiedad. Obtiene o establece el valor que determina si el contenido deStructuredDocumentTag se actualiza antes de guardar.
type: docs
weight: 200
url: /es/net/aspose.words.saving/saveoptions/updatesdtcontent/
---
## SaveOptions.UpdateSdtContent property

Obtiene o establece el valor que determina si el contenido de[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) se actualiza antes de guardar.

```csharp
public bool UpdateSdtContent { get; set; }
```

### Observaciones

El valor predeterminado es`verdadero` .

### Ejemplos

Muestra cómo actualizar etiquetas de documentos estructurados al guardar un documento en PDF.

```csharp
Document doc = new Document();

// Insertar una etiqueta de documento estructurado de lista desplegable.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DropDownList, MarkupLevel.Block);
tag.ListItems.Add(new SdtListItem("Value 1"));
tag.ListItems.Add(new SdtListItem("Value 2"));
tag.ListItems.Add(new SdtListItem("Value 3"));

// La lista desplegable actualmente muestra "Elegir un elemento" como texto predeterminado.
// Establecer la propiedad "SelectedValue" en uno de los elementos de la lista para obtener la etiqueta
// muestra el valor de ese elemento de la lista en lugar del texto predeterminado.
tag.ListItems.SelectedValue = tag.ListItems[1];

doc.FirstSection.Body.AppendChild(tag);

// Crear un objeto "PdfSaveOptions" para pasar al método "Guardar" del documento
// para modificar cómo ese método guarda el documento en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Establecer la propiedad "UpdateSdtContent" en "falso" para no actualizar las etiquetas de documentos estructurados
// mientras guarda el documento en PDF. Mostrarán sus valores predeterminados tal como estaban en el momento de la construcción.
// Establezca la propiedad "UpdateSdtContent" en "true" para asegurarse de que las etiquetas muestren valores actualizados en el PDF.
options.UpdateSdtContent = updateSdtContent;

doc.Save(ArtifactsDir + "StructuredDocumentTag.UpdateSdtContent.pdf", options);
```

### Ver también

* class [SaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../saveoptions/)
* asamblea [Aspose.Words](../../../)


