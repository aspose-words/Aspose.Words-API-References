---
title: "Aspose::Words::Document::RemoveBlankPages metod"
linktitle: "RemoveBlankPages"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::RemoveBlankPages metod. Tar bort tomma sidor från dokumentet i C++."
type: docs
weight: 67500
url: /sv/cpp/aspose.words/document/removeblankpages/
---
## Document::RemoveBlankPages method


Tar bort tomma sidor från dokumentet.

```cpp
System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::Document::RemoveBlankPages()
```


### ReturnValue

Lista med sidnummer har betraktats som tomma och tagits bort.

## Exempel



Visar hur man tar bort tomma sidor från dokumentet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Blank pages.docx");
ASSERT_EQ(2, doc->get_PageCount());
doc->RemoveBlankPages();
doc->UpdatePageLayout();
ASSERT_EQ(1, doc->get_PageCount());
```

## Se även

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
