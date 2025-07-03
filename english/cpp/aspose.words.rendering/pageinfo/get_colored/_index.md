---
title: Aspose::Words::Rendering::PageInfo::get_Colored method
linktitle: get_Colored
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Rendering::PageInfo::get_Colored method. Returns true if the page contains colored content in C++.'
type: docs
weight: 1500
url: /cpp/aspose.words.rendering/pageinfo/get_colored/
---
## PageInfo::get_Colored method


Returns **true** if the page contains colored content.

```cpp
bool Aspose::Words::Rendering::PageInfo::get_Colored()
```


## Examples



Shows how to check whether the page is in color or not. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Check that the first page of the document is not colored.
ASSERT_FALSE(doc->GetPageInfo(0)->get_Colored());
```

## See Also

* Class [PageInfo](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
