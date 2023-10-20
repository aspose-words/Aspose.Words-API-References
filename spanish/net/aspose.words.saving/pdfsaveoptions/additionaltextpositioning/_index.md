---
title: PdfSaveOptions.AdditionalTextPositioning
linktitle: AdditionalTextPositioning
articleTitle: AdditionalTextPositioning
second_title: Aspose.Words para .NET
description: PdfSaveOptions AdditionalTextPositioning propiedad. Un indicador que especifica si se escriben operadores de posicionamiento de texto adicionales o no en C#.
type: docs
weight: 20
url: /es/net/aspose.words.saving/pdfsaveoptions/additionaltextpositioning/
---
## PdfSaveOptions.AdditionalTextPositioning property

Un indicador que especifica si se escriben operadores de posicionamiento de texto adicionales o no.

```csharp
public bool AdditionalTextPositioning { get; set; }
```

## Observaciones

si`verdadero` , se escriben operadores de posicionamiento de texto adicionales en el PDF de salida. Esto puede ayudar a superar los problemas de posicionamiento incorrecto del texto en algunas impresoras. La desventaja es el mayor tamaño del documento PDF.

El valor predeterminado es`FALSO`.

## Ejemplos

Muestre cómo escribir operadores de posicionamiento de texto adicionales.

```csharp
Document doc = new Document(MyDir + "Text positioning operators.docx");

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions
{
    TextCompression = PdfTextCompression.None,

    // Establece la propiedad "AdditionalTextPositioning" en "true" para intentar corregir errores
    // posicionamiento del elemento en el PDF de salida, si lo hubiera, a costa de un mayor tamaño del archivo.
    // Establece la propiedad "AdditionalTextPositioning" en "false" para representar el documento como de costumbre.
    AdditionalTextPositioning = applyAdditionalTextPositioning
};

doc.Save(ArtifactsDir + "PdfSaveOptions.AdditionalTextPositioning.pdf", saveOptions);
```

### Ver también

* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
