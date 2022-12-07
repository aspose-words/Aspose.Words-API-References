---
title: ExtractPages
second_title: Aspose.Words for C++ API Reference
description: Returns the Document object representing specified range of pages.
type: docs
weight: 144
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
auto doc = MakeObject<Document>(MyDir + u"Layout entities.docx");

doc = doc->ExtractPages(0, 2);

doc->Save(ArtifactsDir + u"Document.ExtractPages.docx");
```

## See Also

* Class [Document](../)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
