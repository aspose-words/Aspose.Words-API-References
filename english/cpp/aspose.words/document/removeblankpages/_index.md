---
title: Aspose::Words::Document::RemoveBlankPages method
linktitle: RemoveBlankPages
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::RemoveBlankPages method. Removes blank pages from the document in C++.'
type: docs
weight: 67500
url: /cpp/aspose.words/document/removeblankpages/
---
## Document::RemoveBlankPages method


Removes blank pages from the document.

```cpp
System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::Document::RemoveBlankPages()
```


### ReturnValue

List of page numbers has been considered as blank and removed.

## Examples



Shows how to remove blank pages from the document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Blank pages.docx");
ASSERT_EQ(2, doc->get_PageCount());
doc->RemoveBlankPages();
doc->UpdatePageLayout();
ASSERT_EQ(1, doc->get_PageCount());
```

## See Also

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
