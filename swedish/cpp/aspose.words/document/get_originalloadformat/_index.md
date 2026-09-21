---
title: "Aspose::Words::Document::get_OriginalLoadFormat metod"
linktitle: "get_OriginalLoadFormat"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::get_OriginalLoadFormat metod. Hämtar formatet på det ursprungliga dokumentet som laddades in i detta objekt i C++."
type: docs
weight: 41000
url: /sv/cpp/aspose.words/document/get_originalloadformat/
---
## Document::get_OriginalLoadFormat method


Hämtar formatet för det ursprungliga dokumentet som laddades in i detta objekt.

```cpp
Aspose::Words::LoadFormat Aspose::Words::Document::get_OriginalLoadFormat() const
```

## Anmärkningar


Om du skapade ett nytt tomt dokument, returneras värdet [Doc](../../loadformat/).

## Exempel



Visar hur man hämtar detaljer om ett dokuments inläsningsoperation.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

ASSERT_EQ(get_MyDir() + u"Document.docx", doc->get_OriginalFileName());
ASSERT_EQ(Aspose::Words::LoadFormat::Docx, doc->get_OriginalLoadFormat());
```

## Se även

* Enum [LoadFormat](../../loadformat/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
