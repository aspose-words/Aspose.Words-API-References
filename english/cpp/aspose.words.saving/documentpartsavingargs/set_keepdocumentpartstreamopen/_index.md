---
title: Aspose::Words::Saving::DocumentPartSavingArgs::set_KeepDocumentPartStreamOpen method
linktitle: set_KeepDocumentPartStreamOpen
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::DocumentPartSavingArgs::set_KeepDocumentPartStreamOpen method. Specifies whether Aspose.Words should keep the stream open or close it after saving a document part in C++.'
type: docs
weight: 10000
url: /cpp/aspose.words.saving/documentpartsavingargs/set_keepdocumentpartstreamopen/
---
## DocumentPartSavingArgs::set_KeepDocumentPartStreamOpen method


Specifies whether Aspose.Words should keep the stream open or close it after saving a document part.

```cpp
void Aspose::Words::Saving::DocumentPartSavingArgs::set_KeepDocumentPartStreamOpen(bool value)
```

## Remarks


Default is **false** and Aspose.Words will close the stream you provided in the [DocumentPartStream](../get_documentpartstream/) property after writing a document part into it. Specify **true** to keep the stream open. Please note that the main output stream provided in the call to [Save()](../../../aspose.words/document/save/) or [Save()](../../../aspose.words/document/save/) will never be closed by Aspose.Words even if [KeepDocumentPartStreamOpen](../get_keepdocumentpartstreamopen/) is set to **false**.
## See Also

* Class [DocumentPartSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
