---
title: get_AdditionalTextPositioning
second_title: Aspose.Words for C++ API Reference
description: A flag specifying whether to write additional text positioning operators or not.
type: docs
weight: 40
url: /cpp/aspose.words.saving/pdfsaveoptions/get_additionaltextpositioning/
---
## PdfSaveOptions::get_AdditionalTextPositioning method


A flag specifying whether to write additional text positioning operators or not.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_AdditionalTextPositioning() const
```

## Remarks


If **true**, additional text positioning operators are written to the output PDF. This may help to overcome issues with inaccurate text positioning with some printers. The downside is the increased PDF document size.

The default value is **false**.

## Examples



Show how to write additional text positioning operators. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Text positioning operators.docx");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
auto saveOptions = MakeObject<PdfSaveOptions>();
saveOptions->set_TextCompression(PdfTextCompression::None);
saveOptions->set_AdditionalTextPositioning(applyAdditionalTextPositioning);

doc->Save(ArtifactsDir + u"PdfSaveOptions.AdditionalTextPositioning.pdf", saveOptions);
```

## See Also

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
