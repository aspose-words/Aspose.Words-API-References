---
title: "Aspose::Words::Document::get_PunctuationKerning-metod"
linktitle: "get_PunctuationKerning"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::get_PunctuationKerning‑metod. Anger om kerning tillämpas på både latintext och interpunktion i C++."
type: docs
weight: 44500
url: /sv/cpp/aspose.words/document/get_punctuationkerning/
---
## Document::get_PunctuationKerning method


Anger om kerning gäller både latinsk text och interpunktion.

```cpp
bool Aspose::Words::Document::get_PunctuationKerning()
```


## Exempel



Visar hur man arbetar med kerning som tillämpas på både latintext och interpunktion.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
ASSERT_TRUE(doc->get_PunctuationKerning());
```

## Se även

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
