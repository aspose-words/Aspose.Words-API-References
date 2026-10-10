---
title: "Aspose::Words::DocumentBase::get_Document Methode"
linktitle: "get_Document"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBase::get_Document Methode. Gibt diese Instanz in C++ zurück."
type: docs
weight: 3000
url: /de/cpp/aspose.words/documentbase/get_document/
---
## DocumentBase::get_Document method


Liest diese Instanz.

```cpp
System::SharedPtr<Aspose::Words::DocumentBase> Aspose::Words::DocumentBase::get_Document() const override
```


## Beispiele



Zeigt, wie ein einfaches Dokument erstellt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Neue Document‑Objekte enthalten standardmäßig den minimalen Satz von Knoten
// die erforderlich sind, um Inhalte wie Text und Formen hinzuzufügen: ein Section, ein Body und ein Paragraph.
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Body>>(System::MakeObject<Aspose::Words::Body>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## Siehe auch

* Class [DocumentBase](../)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
