---
title: StructuredDocumentTag.SetUncheckedSymbol
linktitle: SetUncheckedSymbol
articleTitle: SetUncheckedSymbol
second_title: Aspose.Words para .NET
description: StructuredDocumentTag SetUncheckedSymbol método. Establece el símbolo utilizado para representar el estado no marcado de un control de contenido de casilla de verificación en C#.
type: docs
weight: 370
url: /es/net/aspose.words.markup/structureddocumenttag/setuncheckedsymbol/
---
## StructuredDocumentTag.SetUncheckedSymbol method

Establece el símbolo utilizado para representar el estado no marcado de un control de contenido de casilla de verificación.

```csharp
public void SetUncheckedSymbol(int characterCode, string fontName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| characterCode | Int32 | El código de carácter para el símbolo especificado. |
| fontName | String | El nombre de la fuente que contiene el símbolo. |

## Observaciones

Acceder a este método sólo funcionará paraCheckbox Tipos de TDS.

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
