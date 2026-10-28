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
## Remarks

 The resulting document will not contain pages considered to be blank while other content, including numbering, headers/footers and overall layout should remain unchanged. Page is considered to be blank when body of the page have no visible content, for example, empty table having no borders will be considered as invisible and therefore page will be detected as blank. 
## Examples


Shows how to remove blank pages from the document.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Blank pages.docx"));
ASSERT_EQ(2, doc->get_PageCount());
doc->RemoveBlankPages();
doc->UpdatePageLayout();
ASSERT_EQ(1, doc->get_PageCount());
```
## See Also

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
