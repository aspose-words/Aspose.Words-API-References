---
title: Aspose::Words::Layout::LayoutEnumerator::LayoutEnumerator constructor
linktitle: LayoutEnumerator
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Layout::LayoutEnumerator::LayoutEnumerator constructor. Initializes new instance of this class in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.layout/layoutenumerator/layoutenumerator/
---
## LayoutEnumerator::LayoutEnumerator constructor


Initializes new instance of this class.

```cpp
Aspose::Words::Layout::LayoutEnumerator::LayoutEnumerator(const System::SharedPtr<Aspose::Words::Document> &document)
```


| Parameter | Type | Description |
| --- | --- | --- |
| document | const System::SharedPtr\<Aspose::Words::Document\>\& | A document whose page layout model to enumerate. |
## Remarks


If page layout model of the document hasn't been built the enumerator calls [UpdatePageLayout](../../../aspose.words/document/updatepagelayout/) to build it.

Whenever document is updated and new page layout model is created, a new enumerator must be used to access it.

## See Also

* Class [Document](../../../aspose.words/document/)
* Class [LayoutEnumerator](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
