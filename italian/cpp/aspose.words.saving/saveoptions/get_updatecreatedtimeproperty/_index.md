---
title: "Metodo Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty"
linktitle: "get_UpdateCreatedTimeProperty"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty. Ottiene o imposta un valore che determina se la proprietà CreatedTime viene aggiornata prima del salvataggio. Il valore predefinito è false; in C++."
type: docs
weight: 16000
url: /it/cpp/aspose.words.saving/saveoptions/get_updatecreatedtimeproperty/
---
## SaveOptions::get_UpdateCreatedTimeProperty method


Ottiene o imposta un valore che determina se la proprietà [CreatedTime](../../../aspose.words.properties/builtindocumentproperties/get_createdtime/) viene aggiornata prima del salvataggio. Il valore predefinito è **false**;.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty() const
```


## Esempi



Mostra come aggiornare la proprietà "CreatedTime" di un documento durante il salvataggio.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::DateTime createdTime(2019, 12, 20);
doc->get_BuiltInDocumentProperties()->set_CreatedTime(createdTime);

// Questa flag determina se l'ora di creazione, che è una proprietà integrata, viene aggiornata.
// In tal caso, la data dell'operazione di salvataggio più recente del documento
// con questo oggetto SaveOptions passato come parametro viene utilizzato come ora di creazione.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>();
saveOptions->set_UpdateCreatedTimeProperty(isUpdateCreatedTimeProperty);

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.UpdateCreatedTimeProperty.docx", saveOptions);

// Apri il documento salvato, quindi verifica il valore della proprietà.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocSaveOptions.UpdateCreatedTimeProperty.docx");

if (isUpdateCreatedTimeProperty)
{
    ASSERT_NE(createdTime, doc->get_BuiltInDocumentProperties()->get_CreatedTime());
}
else
{
    ASSERT_EQ(createdTime, doc->get_BuiltInDocumentProperties()->get_CreatedTime());
}
```

## Vedi anche

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
