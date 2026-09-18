---
title: "Aspose::Words::Document::get_OriginalLoadFormat-Methode"
linktitle: "get_OriginalLoadFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::get_OriginalLoadFormat-Methode. Gibt das Format des ursprünglichen Dokuments zurück, das in dieses Objekt in C++ geladen wurde."
type: docs
weight: 41000
url: /de/cpp/aspose.words/document/get_originalloadformat/
---
## Document::get_OriginalLoadFormat method


Liest das Format des ursprünglichen Dokuments, das in dieses Objekt geladen wurde.

```cpp
Aspose::Words::LoadFormat Aspose::Words::Document::get_OriginalLoadFormat() const
```

## Hinweise


Wenn Sie ein neues leeres Dokument erstellt haben, wird der Wert [Doc](../../loadformat/) zurückgegeben.

## Beispiele



Zeigt, wie Details des Ladevorgangs eines Dokuments abgerufen werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

ASSERT_EQ(get_MyDir() + u"Document.docx", doc->get_OriginalFileName());
ASSERT_EQ(Aspose::Words::LoadFormat::Docx, doc->get_OriginalLoadFormat());
```

## Siehe auch

* Enum [LoadFormat](../../loadformat/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
