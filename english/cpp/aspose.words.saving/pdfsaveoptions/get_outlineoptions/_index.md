---
title: Aspose::Words::Saving::PdfSaveOptions::get_OutlineOptions method
linktitle: get_OutlineOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PdfSaveOptions::get_OutlineOptions method. Allows to specify outline options in C++.'
type: docs
weight: 25000
url: /cpp/aspose.words.saving/pdfsaveoptions/get_outlineoptions/
---
## PdfSaveOptions::get_OutlineOptions method


Allows to specify outline options.

```cpp
System::SharedPtr<Aspose::Words::Saving::OutlineOptions> Aspose::Words::Saving::PdfSaveOptions::get_OutlineOptions() const
```

## Remarks


Outlines can be created from headings and bookmarks.

For headings outline level is determined by the heading level.

It is possible to set the max heading level to be included into outlines or disable heading outlines at all.

For bookmarks outline level may be set in options as a default value for all bookmarks or as individual values for particular bookmarks.

Also, outlines can be exported to XPS format by using the same [OutlineOptions](./) class. 
## See Also

* Class [OutlineOptions](../../outlineoptions/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
