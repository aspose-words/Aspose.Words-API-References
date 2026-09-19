---
title: "Metodo Aspose::Words::Document::get_Compliance"
linktitle: "get_Compliance"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Document::get_Compliance. Ottiene la versione di conformità OOXML determinata dal contenuto del documento caricato. Ha senso solo per documenti OOXML in C++."
type: docs
weight: 17000
url: /it/cpp/aspose.words/document/get_compliance/
---
## Document::get_Compliance method


Ottiene la versione di conformità OOXML determinata dal contenuto del documento caricato. Ha senso solo per i documenti OOXML.

```cpp
Aspose::Words::Saving::OoxmlCompliance Aspose::Words::Document::get_Compliance()
```

## Note


Se hai creato un nuovo documento vuoto o caricato un documento non OOXML restituisce il valore [Ecma376_2006](../../../aspose.words.saving/ooxmlcompliance/).

## Esempi



Mostra come leggere la versione di conformità Open Office XML di un documento caricato.
```cpp
// La versione di conformità varia tra i documenti creati da diverse versioni di Microsoft Word.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.doc");
ASSERT_EQ(doc->get_Compliance(), Aspose::Words::Saving::OoxmlCompliance::Ecma376_2006);

doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
ASSERT_EQ(doc->get_Compliance(), Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);
```

## Vedi anche

* Enum [OoxmlCompliance](../../../aspose.words.saving/ooxmlcompliance/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
