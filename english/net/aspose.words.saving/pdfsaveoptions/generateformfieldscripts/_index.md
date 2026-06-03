---
title: PdfSaveOptions.GenerateFormFieldScripts
linktitle: GenerateFormFieldScripts
articleTitle: GenerateFormFieldScripts
second_title: Aspose.Words for .NET
description: Generate PDF form field scripts that mimic Microsoft Word form behavior for improved compatibility and user interaction.
type: docs
weight: 190
url: /net/aspose.words.saving/pdfsaveoptions/generateformfieldscripts/
---
## PdfSaveOptions.GenerateFormFieldScripts property

Specifies whether to generate scripts that emulate specific Microsoft Word form field behavior in PDF. Default is `false`.

```csharp
public bool GenerateFormFieldScripts { get; set; }
```

## Remarks

When this option is enabled, the exporter generates PDF JavaScript actions to emulate Microsoft Word form field behavior, such as date and time form fields with formatting and validation rules.

When set to `true`, supported behavior will be exported as PDF JavaScript actions. When set to `false`, no form field scripts will be generated.

Script execution depends on the PDF viewer. Some PDF viewers might ignore scripts, restrict script execution, or require the user to enable JavaScript.

JavaScript actions are prohibited by PDF/A-1, PDF/A-2 and PDF/A-3 compliance. The `false` value will be used automatically in this case.

## Examples

Shows how to enable generation of JavaScript form field scripts for datetime fields when exporting to PDF.

```csharp
Document doc = new Document(MyDir + inputFile);

// Create save options and enable form field scripts.
// Please note that JavaScript actions are prohibited by PDF/A-1, PDF/A-2 and PDF/A-3 compliance.
PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.PreserveFormFields = true;
saveOptions.GenerateFormFieldScripts = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.GenerateFormFieldScriptsDatetime.pdf", saveOptions);
```

### See Also

* class [PdfSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
