---
title: "Aspose::Words::Document::get_PunctuationKerning metodo"
linktitle: "get_PunctuationKerning"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Document::get_PunctuationKerning metodo. Specifica se la kerning si applica sia al testo latino sia alla punteggiatura in C++."
type: docs
weight: 44500
url: /it/cpp/aspose.words/document/get_punctuationkerning/
---
## Document::get_PunctuationKerning method


Specifica se la kerning si applica sia al testo latino sia alla punteggiatura.

```cpp
bool Aspose::Words::Document::get_PunctuationKerning()
```


## Esempi



Mostra come gestire la kerning che si applica sia al testo latino sia alla punteggiatura.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
ASSERT_TRUE(doc->get_PunctuationKerning());
```

## Vedi anche

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
