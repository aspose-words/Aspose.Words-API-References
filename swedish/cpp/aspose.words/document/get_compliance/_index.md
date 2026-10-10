---
title: "Aspose::Words::Document::get_Compliance method"
linktitle: "get_Compliance"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::get_Compliance method. Hämtar OOXML‑kompatibilitetsversionen som bestäms av det inlästa dokumentets innehåll. Är bara meningsfull för OOXML‑dokument i C++."
type: docs
weight: 17000
url: /sv/cpp/aspose.words/document/get_compliance/
---
## Document::get_Compliance method


Hämtar OOXML‑kompatibilitetsversionen som bestäms utifrån det inlästa dokumentets innehåll. Är bara meningsfull för OOXML‑dokument.

```cpp
Aspose::Words::Saving::OoxmlCompliance Aspose::Words::Document::get_Compliance()
```

## Anmärkningar


Om du skapar ett nytt tomt dokument eller laddar ett icke‑OOXML‑dokument returneras värdet [Ecma376_2006](../../../aspose.words.saving/ooxmlcompliance/).

## Exempel



Visar hur man läser ett inläst dokuments Open Office XML‑kompatibilitetsversion.
```cpp
// Kompatibilitetsversionen varierar mellan dokument som skapats av olika versioner av Microsoft Word.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.doc");
ASSERT_EQ(doc->get_Compliance(), Aspose::Words::Saving::OoxmlCompliance::Ecma376_2006);

doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
ASSERT_EQ(doc->get_Compliance(), Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);
```

## Se även

* Enum [OoxmlCompliance](../../../aspose.words.saving/ooxmlcompliance/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
