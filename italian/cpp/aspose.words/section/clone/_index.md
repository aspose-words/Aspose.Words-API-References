---
title: "Aspose::Words::Section::Clone metodo"
linktitle: "Clone"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Section::Clone metodo. Crea un duplicato di questa sezione in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words/section/clone/
---
## Section::Clone method


Crea un duplicato di questa sezione.

```cpp
System::SharedPtr<Aspose::Words::Section> Aspose::Words::Section::Clone()
```


## Esempi



Mostra come aggiungere e rimuovere sezioni in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");

ASSERT_EQ(u"Section 1\x000c" u"Section 2", doc->GetText().Trim());

// Elimina la prima sezione dal documento.
doc->get_Sections()->RemoveAt(0);

ASSERT_EQ(u"Section 2", doc->GetText().Trim());

// Aggiungi una copia di quella che è ora la prima sezione alla fine del documento.
int32_t lastSectionIdx = doc->get_Sections()->get_Count() - 1;
System::SharedPtr<Aspose::Words::Section> newSection = doc->get_Sections()->idx_get(lastSectionIdx)->Clone();
doc->get_Sections()->Add(newSection);

ASSERT_EQ(u"Section 2\x000c" u"Section 2", doc->GetText().Trim());
```

## Vedi anche

* Class [Section](../)
* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
