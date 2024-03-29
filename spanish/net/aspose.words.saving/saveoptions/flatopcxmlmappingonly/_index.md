---
title: SaveOptions.FlatOpcXmlMappingOnly
second_title: Referencia de API de Aspose.Words para .NET
description: SaveOptions propiedad. Obtiene o establece el valor que determina qué formatos de documento pueden ser asignados porXmlMapping . Solo por defectoFlatOpc se permite mapear el formato del documento.
type: docs
weight: 90
url: /es/net/aspose.words.saving/saveoptions/flatopcxmlmappingonly/
---
## SaveOptions.FlatOpcXmlMappingOnly property

Obtiene o establece el valor que determina qué formatos de documento pueden ser asignados por[`XmlMapping`](../../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Solo por defectoFlatOpc se permite mapear el formato del documento.

```csharp
public bool FlatOpcXmlMappingOnly { get; set; }
```

### Observaciones

Esta opción se combina con[`FlatOpcXmlMappingOnly`](../../../aspose.words.loading/loadoptions/flatopcxmlmappingonly/) . Por lo general, debe establecer ambos en falso para permitir que se asignen formatos de documentos arbitrarios.

### Ejemplos

Muestra cómo vincular etiquetas de documentos estructurados a cualquier formato.

```csharp
// Si es verdadero, SDT contendrá texto HTML sin procesar.
// Si es falso, el HTML asignado se analizará y el documento resultante se insertará en el contenido de SDT.
LoadOptions loadOptions = new LoadOptions { FlatOpcXmlMappingOnly = isFlatOpcXmlMappingOnly };
Document doc = new Document(MyDir + "Structured document tag with HTML content.docx", loadOptions);

SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);
saveOptions.FlatOpcXmlMappingOnly = isFlatOpcXmlMappingOnly;

doc.Save(ArtifactsDir + "LoadOptions.FlatOpcXmlMappingOnly.pdf", saveOptions);
```

### Ver también

* class [SaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../saveoptions/)
* asamblea [Aspose.Words](../../../)


