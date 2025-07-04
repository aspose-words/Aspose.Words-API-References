---
title: Aspose::Words::Document::GetPageInfo method
linktitle: GetPageInfo
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::GetPageInfo method. Gets the page size, orientation and other information about a page that might be useful for printing or rendering in C++.'
type: docs
weight: 62000
url: /cpp/aspose.words/document/getpageinfo/
---
## Document::GetPageInfo method


Gets the page size, orientation and other information about a page that might be useful for printing or rendering.

```cpp
System::SharedPtr<Aspose::Words::Rendering::PageInfo> Aspose::Words::Document::GetPageInfo(int32_t pageIndex)
```


| Parameter | Type | Description |
| --- | --- | --- |
| pageIndex | int32_t | The 0-based page index. |

## Examples



Shows how to check whether the page is in color or not. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Check that the first page of the document is not colored.
ASSERT_FALSE(doc->GetPageInfo(0)->get_Colored());
```

## See Also

* Class [PageInfo](../../../aspose.words.rendering/pageinfo/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
