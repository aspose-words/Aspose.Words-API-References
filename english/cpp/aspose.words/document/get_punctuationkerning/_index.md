---
title: Aspose::Words::Document::get_PunctuationKerning method
linktitle: get_PunctuationKerning
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::get_PunctuationKerning method. Specifies whether kerning applies to both Latin text and punctuation in C++.'
type: docs
weight: 44500
url: /cpp/aspose.words/document/get_punctuationkerning/
---
## Document::get_PunctuationKerning method


Specifies whether kerning applies to both Latin text and punctuation.

```cpp
bool Aspose::Words::Document::get_PunctuationKerning()
```


## Examples



Shows how to work with kerning applies to both Latin text and punctuation. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
ASSERT_TRUE(doc->get_PunctuationKerning());
```

## See Also

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
