---
title: "Aspose::Words::Document::get_Compliance method"
linktitle: "get_Compliance"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::get_Compliance-Methode. Ruft die OOXML-Konformitätsversion ab, die aus dem geladenen Dokumentinhalt ermittelt wird. Sinnvoll nur für OOXML-Dokumente in C++."
type: docs
weight: 17000
url: /de/cpp/aspose.words/document/get_compliance/
---
## Document::get_Compliance method


Liest die OOXML‑Konformitätsversion, die aus dem geladenen Dokumentinhalt ermittelt wird. Sinnvoll nur für OOXML‑Dokumente.

```cpp
Aspose::Words::Saving::OoxmlCompliance Aspose::Words::Document::get_Compliance()
```

## Hinweise


Wenn Sie ein neues leeres Dokument erstellt oder ein nicht-OOXML-Dokument geladen haben, wird der [Ecma376_2006](../../../aspose.words.saving/ooxmlcompliance/) Wert zurückgegeben.

## Beispiele



Zeigt, wie die Open Office XML-Konformitätsversion eines geladenen Dokuments gelesen wird.
```cpp
// Die Konformitätsversion variiert zwischen Dokumenten, die mit verschiedenen Versionen von Microsoft Word erstellt wurden.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.doc");
ASSERT_EQ(doc->get_Compliance(), Aspose::Words::Saving::OoxmlCompliance::Ecma376_2006);

doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
ASSERT_EQ(doc->get_Compliance(), Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);
```

## Siehe auch

* Enum [OoxmlCompliance](../../../aspose.words.saving/ooxmlcompliance/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
