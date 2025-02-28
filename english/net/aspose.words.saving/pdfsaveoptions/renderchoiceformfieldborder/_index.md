---
title: PdfSaveOptions.RenderChoiceFormFieldBorder
linktitle: RenderChoiceFormFieldBorder
articleTitle: RenderChoiceFormFieldBorder
second_title: Aspose.Words for .NET
description: Discover how the PdfSaveOptions RenderChoiceFormFieldBorder property enhances PDF form design by controlling choice field borders for better user experience.
type: docs
weight: 290
url: /net/aspose.words.saving/pdfsaveoptions/renderchoiceformfieldborder/
---
## PdfSaveOptions.RenderChoiceFormFieldBorder property

Specifies whether to render PDF choice form field border.

```csharp
public bool RenderChoiceFormFieldBorder { get; set; }
```

## Remarks

PDF choice form fields are used for export of SDT Combo Box Content Control, SDT Drop-Down List Content Control and legacy Drop-Down Form Field when [`PreserveFormFields`](../preserveformfields/) option is enabled.

The default value is `true`.

## Examples

Shows how to render PDF choice form field border.

```csharp
Document doc = new Document(MyDir + "Legacy drop-down.docx");

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.PreserveFormFields = true;
saveOptions.RenderChoiceFormFieldBorder = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderChoiceFormFieldBorder.pdf", saveOptions);
```

### See Also

* class [PdfSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
