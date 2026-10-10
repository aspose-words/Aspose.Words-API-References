---
title: "Aspose::Words::Saving::TxtSaveOptionsBase::get_ForcePageBreaks metodo"
linktitle: "get_ForcePageBreaks"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::TxtSaveOptionsBase::get_ForcePageBreaks metodo. Consente di specificare se le interruzioni di pagina devono essere conservate durante l'esportazione. Il valore predefinito è false in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.saving/txtsaveoptionsbase/get_forcepagebreaks/
---
## TxtSaveOptionsBase::get_ForcePageBreaks method


Consente di specificare se le interruzioni di pagina devono essere conservate durante l'esportazione. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Saving::TxtSaveOptionsBase::get_ForcePageBreaks() const
```


## Esempi



Mostra come specificare se conservare le interruzioni di pagina durante l'esportazione di un documento in testo semplice.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Page 1");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3");

// Crea un oggetto "TxtSaveOptions", che possiamo passare al metodo "Save" del documento
// metodo per modificare il modo in cui salviamo il documento in testo semplice.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// Gli oggetti "Document" di Aspose.Words hanno interruzioni di pagina, proprio come i documenti Microsoft Word.
// I formati di salvataggio come ".txt" sono un unico corpo continuo di testo senza interruzioni di pagina.
// Imposta la proprietà "ForcePageBreaks" su "true" per conservare tutte le interruzioni di pagina nella forma del carattere "\\f".
// Imposta la proprietà "ForcePageBreaks" su "false" per scartare tutte le interruzioni di pagina.
saveOptions->set_ForcePageBreaks(forcePageBreaks);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.PageBreaks.txt", saveOptions);

// Se carichiamo un documento di testo semplice con interruzioni di pagina,
// l'oggetto "Document" le utilizzerà per suddividere il corpo in pagine.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"TxtSaveOptions.PageBreaks.txt");

ASSERT_EQ(forcePageBreaks ? 3 : 1, doc->get_PageCount());
```

## Vedi anche

* Class [TxtSaveOptionsBase](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
