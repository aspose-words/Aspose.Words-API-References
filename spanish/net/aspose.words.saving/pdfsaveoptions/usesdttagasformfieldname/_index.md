---
title: PdfSaveOptions.UseSdtTagAsFormFieldName
linktitle: UseSdtTagAsFormFieldName
articleTitle: UseSdtTagAsFormFieldName
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad PdfSaveOptions UseSdtTagAsFormFieldName mejora los formularios PDF al utilizar etiquetas de control SDT para una mejor organización y claridad.
type: docs
weight: 340
url: /es/net/aspose.words.saving/pdfsaveoptions/usesdttagasformfieldname/
---
## PdfSaveOptions.UseSdtTagAsFormFieldName property

Especifica si se debe utilizar la etiqueta de control SDT o la propiedad Id como nombre de un campo de formulario en PDF.

```csharp
public bool UseSdtTagAsFormFieldName { get; set; }
```

## Observaciones

El valor predeterminado es`FALSO`.

Cuando se establece en`FALSO`La propiedad Id del control SDT se utiliza como nombre de un campo de formulario en PDF.

Cuando se establece en`verdadero`La propiedad de etiqueta de control SDT se utiliza como nombre de un campo de formulario en PDF.

Si se establece en`verdadero` y la etiqueta está vacía, la propiedad Id se utilizará como nombre de campo de formulario.

Si se establece en`verdadero` y los valores de etiqueta no son únicos, los valores de etiqueta duplicados se modificarán para crear nombres de campos de formulario PDF únicos.

## Ejemplos

Muestra cómo utilizar la propiedad Id o etiqueta de control SDT como nombre de un campo de formulario en PDF.

```csharp
Document doc = new Document(MyDir + "Form fields.docx");

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.PreserveFormFields = true;
// Cuando se establece en 'falso', la propiedad Id del control SDT se utiliza como nombre de un campo de formulario en PDF.
// Cuando se establece en 'verdadero', la propiedad de etiqueta de control SDT se utiliza como nombre de un campo de formulario en PDF.
saveOptions.UseSdtTagAsFormFieldName = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.SdtTagAsFormFieldName.pdf", saveOptions);
```

### Ver también

* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
