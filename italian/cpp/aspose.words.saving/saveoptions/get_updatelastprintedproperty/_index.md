---
title: "Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty metodo"
linktitle: "get_UpdateLastPrintedProperty"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty metodo. Ottiene o imposta un valore che determina se la proprietà LastPrinted viene aggiornata prima del salvataggio in C++."
type: docs
weight: 18000
url: /it/cpp/aspose.words.saving/saveoptions/get_updatelastprintedproperty/
---
## SaveOptions::get_UpdateLastPrintedProperty method


Ottiene o imposta un valore che determina se la proprietà [LastPrinted](../../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) viene aggiornata prima del salvataggio.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty() const
```


## Esempi



Mostra come aggiornare la proprietà "Last printed" di un documento durante il salvataggio.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::DateTime lastPrinted(2019, 12, 20);
doc->get_BuiltInDocumentProperties()->set_LastPrinted(lastPrinted);

// Questa flag determina se la data di ultima stampa, che è una proprietà incorporata, viene aggiornata.
// In tal caso, la data dell'operazione di salvataggio più recente del documento
// con questo oggetto SaveOptions passato come parametro viene utilizzata come data di stampa.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>();
saveOptions->set_UpdateLastPrintedProperty(isUpdateLastPrintedProperty);

// In Microsoft Word 2003, questa proprietà può essere trovata tramite File -> Proprietà -> Statistiche -> Stampato.
// Può anche essere visualizzata nel corpo del documento utilizzando un campo PRINTDATE.
doc->Save(get_ArtifactsDir() + u"DocSaveOptions.UpdateLastPrintedProperty.doc", saveOptions);

// Apri il documento salvato, quindi verifica il valore della proprietà.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocSaveOptions.UpdateLastPrintedProperty.doc");

if (isUpdateLastPrintedProperty)
{
    ASSERT_NE(lastPrinted, doc->get_BuiltInDocumentProperties()->get_LastPrinted());
}
else
{
    ASSERT_EQ(lastPrinted, doc->get_BuiltInDocumentProperties()->get_LastPrinted());
}
```

## Vedi anche

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
