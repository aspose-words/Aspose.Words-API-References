---
title: Aspose::Words::Document::get_VersionsCount method
linktitle: get_VersionsCount
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::get_VersionsCount method. Gets the number of document versions that was stored in the DOC document in C++.'
type: docs
weight: 57000
url: /cpp/aspose.words/document/get_versionscount/
---
## Document::get_VersionsCount method


Gets the number of document versions that was stored in the DOC document.

```cpp
int32_t Aspose::Words::Document::get_VersionsCount()
```

## Remarks


Versions in Microsoft Word are accessed via the File/Versions menu. Microsoft Word supports versions only for DOC files.

This property allows to detect if there were document versions stored in this document before it was opened in Aspose.Words. Aspose.Words provides no other support for document versions. If you save this document using Aspose.Words, the document will be saved without versions.

## Examples



Shows how to work with the versions count feature of older Microsoft Word documents. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Versions.doc");

// We can read this property of a document, but we cannot preserve it while saving.
ASSERT_EQ(4, doc->get_VersionsCount());

doc->Save(get_ArtifactsDir() + u"Document.VersionsCount.doc");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.VersionsCount.doc");

ASSERT_EQ(0, doc->get_VersionsCount());
```

## See Also

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
