---
title: get_Text
second_title: Aspose.Words for C++ API Reference
description: Gets the text of the range.
type: docs
weight: 79
url: /cpp/aspose.words/range/get_text/
---
## Range::get_Text method


Gets the text of the range.

```cpp
System::String Aspose::Words::Range::get_Text()
```

## Remarks


The returned string includes all control and special characters as described in [ControlChar](../../controlchar/).

## Examples



Shows how to get the text contents of all the nodes that a range covers. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Write(u"Hello world!");

ASSERT_EQ(u"Hello world!", doc->get_Range()->get_Text().Trim());
```

## See Also

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
