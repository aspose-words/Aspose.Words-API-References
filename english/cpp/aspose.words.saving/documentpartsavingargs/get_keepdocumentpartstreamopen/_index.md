---
title: Aspose::Words::Saving::DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen method
linktitle: get_KeepDocumentPartStreamOpen
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen method. Specifies whether Aspose.Words should keep the stream open or close it after saving a document part in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.saving/documentpartsavingargs/get_keepdocumentpartstreamopen/
---
## DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen method


Specifies whether Aspose.Words should keep the stream open or close it after saving a document part.

```cpp
bool Aspose::Words::Saving::DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen() const
```

## Remarks


Default is **false** and Aspose.Words will close the stream you provided in the [DocumentPartStream](../get_documentpartstream/) property after writing a document part into it. Specify **true** to keep the stream open. Please note that the main output stream provided in the call to [Save()](../) or [Save()](../) will never be closed by Aspose.Words even if [KeepDocumentPartStreamOpen](./) is set to **false**.

## See Also

* Class [DocumentPartSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
