---
title: StructuredDocumentTag.SetCheckedSymbol
linktitle: SetCheckedSymbol
articleTitle: SetCheckedSymbol
second_title: Aspose.Words para .NET
description: Descubra cómo utilizar el método SetCheckedSymbol en StructuredDocumentTag para personalizar los elementos visuales de las casillas de verificación y mejorar la experiencia del usuario.
type: docs
weight: 380
url: /es/net/aspose.words.markup/structureddocumenttag/setcheckedsymbol/
---
## StructuredDocumentTag.SetCheckedSymbol method

Establece el símbolo utilizado para representar el estado marcado de un control de contenido de casilla de verificación.

```csharp
public void SetCheckedSymbol(int characterCode, string fontName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| characterCode | Int32 | El código de carácter para el símbolo especificado. |
| fontName | String | El nombre de la fuente que contiene el símbolo. |

## Observaciones

Acceder a este método solo funcionará paraCheckbox Tipos de SDT.

Para todos los demás tipos de SDT se producirá una excepción.

## Ejemplos

Muestra cómo crear una etiqueta de documento estructurado en forma de casilla de verificación.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

StructuredDocumentTag sdtCheckBox =
    new StructuredDocumentTag(doc, SdtType.Checkbox, MarkupLevel.Inline) { Checked = true };

// Podemos configurar los símbolos utilizados para representar el estado marcado/desmarcado de un control de contenido de casilla de verificación.
sdtCheckBox.SetCheckedSymbol(0x00A9, "Times New Roman");
sdtCheckBox.SetUncheckedSymbol(0x00AE, "Times New Roman");

builder.InsertNode(sdtCheckBox);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CheckBox.docx");
```

### Ver también

* class [StructuredDocumentTag](../)
* espacio de nombres [Aspose.Words.Markup](../../../aspose.words.markup/)
* asamblea [Aspose.Words](../../../)
