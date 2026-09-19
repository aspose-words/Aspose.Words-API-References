---
title: "Aspose::Words::ImportFormatOptions::get_AppendDocumentWithNewPage metodo"
linktitle: "get_AppendDocumentWithNewPage"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::ImportFormatOptions::get_AppendDocumentWithNewPage metodo. Ottiene o imposta un valore booleano che indica se modificare il tipo della prima sezione importata in NewPage forzatamente quando si chiama AppendDocument(). Il valore predefinito è true in C++."
type: docs
weight: 3500
url: /it/cpp/aspose.words/importformatoptions/get_appenddocumentwithnewpage/
---
## ImportFormatOptions::get_AppendDocumentWithNewPage method


Ottiene o imposta un valore booleano che indica se modificare il tipo della prima sezione importata in [NewPage](../../sectionstart/) forzatamente quando si chiama [AppendDocument()](../). Il valore predefinito è **true**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_AppendDocumentWithNewPage() const
```


## Esempi



Mostra come preservare il tipo di sezione originale.
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
auto srcDoc = System::MakeObject<Aspose::Words::Document>();

srcDoc->get_FirstSection()->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::Continuous);

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_AppendDocumentWithNewPage(false);
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

ASSERT_EQ(Aspose::Words::SectionStart::Continuous, dstDoc->get_Sections()->idx_get(1)->get_PageSetup()->get_SectionStart());
```

## Vedi anche

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
