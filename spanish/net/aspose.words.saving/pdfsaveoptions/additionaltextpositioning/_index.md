---
title: PdfSaveOptions.AdditionalTextPositioning
linktitle: AdditionalTextPositioning
articleTitle: AdditionalTextPositioning
second_title: Aspose.Words para .NET
description: Descubre la propiedad PdfSaveOptions FurtherTextPositioning para controlar la posición del texto en archivos PDF. ¡Mejora el diseño de tu documento fácilmente!
type: docs
weight: 20
url: /es/net/aspose.words.saving/pdfsaveoptions/additionaltextpositioning/
---
## PdfSaveOptions.AdditionalTextPositioning property

Un indicador que especifica si se deben escribir operadores de posicionamiento de texto adicionales o no.

```csharp
public bool AdditionalTextPositioning { get; set; }
```

## Observaciones

Si`verdadero` Se añaden operadores de posicionamiento de texto adicionales al PDF de salida. Esto puede ayudar a solucionar problemas de posicionamiento de texto impreciso en algunas impresoras. La desventaja es el aumento del tamaño del documento PDF.

El valor predeterminado es`FALSO`.

## Ejemplos

Muestra cómo escribir operadores de posicionamiento de texto adicionales.

```csharp
Document doc = new Document(MyDir + "Text positioning operators.docx");

// Crea un objeto "PdfSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions
{
    TextCompression = PdfTextCompression.None,

    // Establezca la propiedad "AdditionalTextPositioning" en "verdadero" para intentar corregir errores
    // posicionamiento de los elementos en el PDF de salida, si los hubiera, a costa de aumentar el tamaño del archivo.
    // Establezca la propiedad "AdditionalTextPositioning" en "falso" para representar el documento como de costumbre.
    AdditionalTextPositioning = applyAdditionalTextPositioning
};

doc.Save(ArtifactsDir + "PdfSaveOptions.AdditionalTextPositioning.pdf", saveOptions);
```

### Ver también

* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
