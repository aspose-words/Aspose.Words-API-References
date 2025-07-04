---
title: Aspose::Words::Document::ExtractPages method
linktitle: ExtractPages
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::ExtractPages method. Returns the Document object representing specified range of pages in C++.'
type: docs
weight: 12000
url: /cpp/aspose.words/document/extractpages/
---
## Document::ExtractPages method


Returns the [Document](../) object representing specified range of pages.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::Document::ExtractPages(int32_t index, int32_t count)
```


| Parameter | Type | Description |
| --- | --- | --- |
| index | int32_t | The zero-based index of the first page to extract. |
| count | int32_t | Number of pages to be extracted. |

## Examples



Shows how to get specified range of pages from the document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Layout entities.docx");

doc = doc->ExtractPages(0, 2);

doc->Save(get_ArtifactsDir() + u"Document.ExtractPages.docx");
```

## See Also

* Class [Document](../)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
