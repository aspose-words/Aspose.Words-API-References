---
title: "Aspose::Words::ImportFormatOptions::get_AppendDocumentWithNewPage Methode"
linktitle: "get_AppendDocumentWithNewPage"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ImportFormatOptions::get_AppendDocumentWithNewPage Methode. Gibt einen booleschen Wert zurück oder legt ihn fest, der angibt, ob der Typ des zuerst importierten Abschnitts beim Aufruf von AppendDocument() zwingend in NewPage geändert werden soll. Der Standardwert ist true in C++."
type: docs
weight: 3500
url: /de/cpp/aspose.words/importformatoptions/get_appenddocumentwithnewpage/
---
## ImportFormatOptions::get_AppendDocumentWithNewPage method


Gibt einen booleschen Wert zurück oder legt ihn fest, der angibt, ob der Typ des zuerst importierten Abschnitts beim Aufruf von [AppendDocument()](../) zwingend zu [NewPage](../../sectionstart/) geändert werden soll. Der Standardwert ist **true**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_AppendDocumentWithNewPage() const
```


## Beispiele



Zeigt, wie man den ursprünglichen Abschnittstyp beibehält.
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
auto srcDoc = System::MakeObject<Aspose::Words::Document>();

srcDoc->get_FirstSection()->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::Continuous);

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_AppendDocumentWithNewPage(false);
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

ASSERT_EQ(Aspose::Words::SectionStart::Continuous, dstDoc->get_Sections()->idx_get(1)->get_PageSetup()->get_SectionStart());
```

## Siehe auch

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
