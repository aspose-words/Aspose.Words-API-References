---
title: "Aspose::Words::Tables::RowFormat::get_AllowBreakAcrossPages method"
linktitle: "get_AllowBreakAcrossPages"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Tables::RowFormat::get_AllowBreakAcrossPages method. True se il testo in una riga di tabella è consentito di dividersi attraverso un'interruzione di pagina in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.tables/rowformat/get_allowbreakacrosspages/
---
## RowFormat::get_AllowBreakAcrossPages method


Vero se il testo in una riga di tabella è consentito di dividersi attraverso un'interruzione di pagina.

```cpp
bool Aspose::Words::Tables::RowFormat::get_AllowBreakAcrossPages()
```


## Esempi



Mostra come disabilitare la divisione delle righe tra pagine per ogni riga in una tabella.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table spanning two pages.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Imposta la proprietà "AllowBreakAcrossPages" su "false" per mantenere la riga
// intatta se una tabella copre due pagine, che altrimenti si spezzerebbe lungo quella riga.
// Se la riga è troppo grande per stare in una pagina, Microsoft Word la sposterà alla pagina successiva.
// Imposta la proprietà "AllowBreakAcrossPages" su "true" per consentire alla riga di dividersi tra due pagine.
for (auto&& row : System::IterateOver<Aspose::Words::Tables::Row>(table))
{
    row->get_RowFormat()->set_AllowBreakAcrossPages(allowBreakAcrossPages);
}

doc->Save(get_ArtifactsDir() + u"Table.AllowBreakAcrossPages.docx");
```

## Vedi anche

* Class [RowFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
