---
title: StructuredDocumentTag.StructuredDocumentTag
second_title: Referencia de API de Aspose.Words para .NET
description: StructuredDocumentTag constructor. Inicializa una nueva instancia del Etiqueta de documento estructurado clase.
type: docs
weight: 10
url: /es/net/aspose.words.markup/structureddocumenttag/structureddocumenttag/
---
## StructuredDocumentTag constructor

Inicializa una nueva instancia del **Etiqueta de documento estructurado** clase.

```csharp
public StructuredDocumentTag(DocumentBase doc, SdtType type, MarkupLevel level)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| doc | DocumentBase | El documento del propietario. |
| type | SdtType | Tipo de nodo SDT. |
| level | MarkupLevel | Nivel de nodo SDT dentro del documento. |

### Observaciones

Se pueden crear los siguientes tipos de SDT:

* Checkbox
* DropDownList
* ComboBox
* Date
* BuildingBlockGallery
* Group
* Picture
* RichText
* PlainText

### Ejemplos

Muestre cómo crear una etiqueta de documento estructurado en forma de casilla de verificación.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

StructuredDocumentTag sdtCheckBox =
    new StructuredDocumentTag(doc, SdtType.Checkbox, MarkupLevel.Inline) {Checked = true};

// Podemos establecer los símbolos utilizados para representar el estado marcado/no marcado de un control de contenido de casilla de verificación.
sdtCheckBox.SetCheckedSymbol(0x00A9, "Times New Roman");
sdtCheckBox.SetUncheckedSymbol(0x00AE, "Times New Roman");

builder.InsertNode(sdtCheckBox);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CheckBox.docx");
```

### Ver también

* class [DocumentBase](../../../aspose.words/documentbase/)
* enum [SdtType](../../sdttype/)
* enum [MarkupLevel](../../markuplevel/)
* class [StructuredDocumentTag](../)
* espacio de nombres [Aspose.Words.Markup](../../structureddocumenttag/)
* asamblea [Aspose.Words](../../../)


