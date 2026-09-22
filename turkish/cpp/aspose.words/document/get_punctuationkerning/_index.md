---
title: "Aspose::Words::Document::get_PunctuationKerning yöntemi"
linktitle: "get_PunctuationKerning"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::get_PunctuationKerning yöntemi. C++'ta kerning'in hem Latin metnine hem de noktalama işaretlerine uygulanıp uygulanmayacağını belirler."
type: docs
weight: 44500
url: /tr/cpp/aspose.words/document/get_punctuationkerning/
---
## Document::get_PunctuationKerning method


Kerning'in hem Latin metnine hem de noktalama işaretlerine uygulanıp uygulanmayacağını belirtir.

```cpp
bool Aspose::Words::Document::get_PunctuationKerning()
```


## Örnekler



Kerning'in hem Latin metnine hem de noktalama işaretlerine uygulanmasını nasıl çalıştıracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
ASSERT_TRUE(doc->get_PunctuationKerning());
```

## Ayrıca Bakınız

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
