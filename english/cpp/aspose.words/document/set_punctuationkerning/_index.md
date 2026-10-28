---
title: Aspose::Words::Document::set_PunctuationKerning method
linktitle: set_PunctuationKerning
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::set_PunctuationKerning method. Specifies whether kerning applies to both Latin text and punctuation in C++.'
type: docs
weight: 165000
url: /cpp/aspose.words/document/set_punctuationkerning/
---
## Document::set_PunctuationKerning method


Specifies whether kerning applies to both Latin text and punctuation.

```cpp
void Aspose::Words::Document::set_PunctuationKerning(bool value)
```

## Examples


Shows how to work with kerning applies to both Latin text and punctuation.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Document.docx"));
ASSERT_TRUE(doc->get_PunctuationKerning());
```
## See Also

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
