---
title: PdfSaveOptions.UseSdtTagAsFormFieldName
linktitle: UseSdtTagAsFormFieldName
articleTitle: UseSdtTagAsFormFieldName
second_title: Aspose.Words for .NET
description: Discover how the PdfSaveOptions UseSdtTagAsFormFieldName property enhances PDF forms by using SDT control tags for better organization and clarity.
type: docs
weight: 350
url: /net/aspose.words.saving/pdfsaveoptions/usesdttagasformfieldname/
---
## PdfSaveOptions.UseSdtTagAsFormFieldName property

Specifies whether to use SDT control Tag or Id property as a name of form field in PDF.

```csharp
public bool UseSdtTagAsFormFieldName { get; set; }
```

## Remarks

The default value is `false`.

When set to `false`, SDT control Id property is used as a name of form field in PDF.

When set to `true`, SDT control Tag property is used as a name of form field in PDF.

If set to `true` and Tag is empty, Id property will be used as a form field name.

If set to `true` and Tag values are not unique, duplicate Tag values will be altered to build unique PDF form field names.

## Examples

Shows how to use SDT control Tag or Id property as a name of form field in PDF.

```csharp
Document doc = new Document(MyDir + "Form fields.docx");

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.PreserveFormFields = true;
// When set to 'false', SDT control Id property is used as a name of form field in PDF.
// When set to 'true', SDT control Tag property is used as a name of form field in PDF.
saveOptions.UseSdtTagAsFormFieldName = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.SdtTagAsFormFieldName.pdf", saveOptions);
```

### See Also

* class [PdfSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
