---
title: "Aspose::Words::Document::get_PunctuationKerning-Methode"
linktitle: "get_PunctuationKerning"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::get_PunctuationKerning-Methode. Gibt an, ob Kerning sowohl für lateinischen Text als auch für Interpunktion in C++ angewendet wird."
type: docs
weight: 44500
url: /de/cpp/aspose.words/document/get_punctuationkerning/
---
## Document::get_PunctuationKerning method


Gibt an, ob Kerning sowohl auf lateinischen Text als auch auf Interpunktion angewendet wird.

```cpp
bool Aspose::Words::Document::get_PunctuationKerning()
```


## Beispiele



Zeigt, wie man mit Kerning arbeitet, das sowohl für lateinischen Text als auch für Interpunktion gilt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
ASSERT_TRUE(doc->get_PunctuationKerning());
```

## Siehe auch

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
