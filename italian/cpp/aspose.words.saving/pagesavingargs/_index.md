---
title: "classe Aspose::Words::Saving::PageSavingArgs"
linktitle: "PageSavingArgs"
second_title: "Riferimento API Aspose.Words per C++"
description: "classe Aspose::Words::Saving::PageSavingArgs. Fornisce dati per l'evento PageSaving(). Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 19000
url: /it/cpp/aspose.words.saving/pagesavingargs/
---
## PageSavingArgs class


Fornisce dati per l'evento [PageSaving()](../ipagesavingcallback/pagesaving/). Per saperne di più, visita l'articolo della documentazione [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class PageSavingArgs : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_KeepPageStreamOpen](./get_keeppagestreamopen/)() const | Specifica se Aspose.Words deve mantenere lo stream aperto o chiuderlo dopo il salvataggio di una pagina del documento. |
| [get_PageFileName](./get_pagefilename/)() const | Ottiene il nome file in cui verrà salvata la pagina del documento. |
| [get_PageIndex](./get_pageindex/)() const | Indice della pagina corrente. |
| [get_PageStream](./get_pagestream/)() const | Consente di specificare lo stream in cui verrà salvata la pagina del documento. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PageSavingArgs](./pagesavingargs/)() |  |
| [set_KeepPageStreamOpen](./set_keeppagestreamopen/)(bool) | Impostatore per [Aspose::Words::Saving::PageSavingArgs::get_KeepPageStreamOpen](./get_keeppagestreamopen/). |
| [set_PageFileName](./set_pagefilename/)(const System::String\&) | Imposta il nome file in cui verrà salvata la pagina del documento. |
| [set_PageStream](./set_pagestream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Impostatore per [Aspose::Words::Saving::PageSavingArgs::get_PageStream](./get_pagestream/). |
| [set_PageStream](./set_pagestream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| static [Type](./type/)() |  |
## Vedi anche

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
