---
title: StructuredDocumentTag.Checked
linktitle: Checked
articleTitle: Checked
second_title: Aspose.Words para .NET
description: StructuredDocumentTag Checked propiedad. Obtiene/establece el estado actual de la casilla de verificaciónTED . El valor predeterminado para esta propiedad esFALSO  en C#.
type: docs
weight: 60
url: /es/net/aspose.words.markup/structureddocumenttag/checked/
---
## StructuredDocumentTag.Checked property

Obtiene/establece el estado actual de la casilla de verificación**TED** . El valor predeterminado para esta propiedad es`FALSO` .

```csharp
public bool Checked { get; set; }
```

## Observaciones

Acceder a esta propiedad sólo funcionará paraCheckbox Tipos SDT.

Para todos los demás tipos de SDT se producirá una excepción.

## Ejemplos

Muestre cómo crear una etiqueta de documento estructurada en forma de casilla de verificación.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

StructuredDocumentTag sdtCheckBox =
    new StructuredDocumentTag(doc, SdtType.Checkbox, MarkupLevel.Inline) {Checked = true};

// Podemos configurar los símbolos utilizados para representar el estado marcado/no marcado de un control de contenido de casilla de verificación.
sdtCheckBox.SetCheckedSymbol(0x00A9, "Times New Roman");
sdtCheckBox.SetUncheckedSymbol(0x00AE, "Times New Roman");

builder.InsertNode(sdtCheckBox);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CheckBox.docx");
```

### Ver también

* class [StructuredDocumentTag](../)
* espacio de nombres [Aspose.Words.Markup](../../../aspose.words.markup/)
* asamblea [Aspose.Words](../../../)
