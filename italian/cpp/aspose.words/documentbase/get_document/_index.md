---
title: "Metodo Aspose::Words::DocumentBase::get_Document"
linktitle: "get_Document"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::DocumentBase::get_Document. Ottiene questa istanza in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words/documentbase/get_document/
---
## DocumentBase::get_Document method


Ottiene questa istanza.

```cpp
System::SharedPtr<Aspose::Words::DocumentBase> Aspose::Words::DocumentBase::get_Document() const override
```


## Esempi



Mostra come creare un documento semplice.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// I nuovi oggetti Document per impostazione predefinita includono il set minimo di nodi
// necessari per iniziare ad aggiungere contenuti come testo e forme: una Section, un Body e un Paragraph.
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Body>>(System::MakeObject<Aspose::Words::Body>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## Vedi anche

* Class [DocumentBase](../)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
