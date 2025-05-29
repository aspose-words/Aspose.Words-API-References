---
title: PdfSaveOptions.RenderChoiceFormFieldBorder
linktitle: RenderChoiceFormFieldBorder
articleTitle: RenderChoiceFormFieldBorder
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad PdfSaveOptions RenderChoiceFormFieldBorder mejora el diseño del formulario PDF al controlar los bordes del campo de opción para una mejor experiencia del usuario.
type: docs
weight: 290
url: /es/net/aspose.words.saving/pdfsaveoptions/renderchoiceformfieldborder/
---
## PdfSaveOptions.RenderChoiceFormFieldBorder property

Especifica si se debe representar el borde del campo de opción del formulario PDF.

```csharp
public bool RenderChoiceFormFieldBorder { get; set; }
```

## Observaciones

Los campos de formulario de elección de PDF se utilizan para exportar el control de contenido del cuadro combinado SDT, el control Content de lista desplegable SDT y el campo de formulario desplegable heredado cuando[`PreserveFormFields`](../preserveformfields/) La opción está habilitada.

El valor predeterminado es`verdadero`.

## Ejemplos

Muestra cómo representar el borde del campo de opción del formulario PDF.

```csharp
Document doc = new Document(MyDir + "Legacy drop-down.docx");

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.PreserveFormFields = true;
saveOptions.RenderChoiceFormFieldBorder = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderChoiceFormFieldBorder.pdf", saveOptions);
```

### Ver también

* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
