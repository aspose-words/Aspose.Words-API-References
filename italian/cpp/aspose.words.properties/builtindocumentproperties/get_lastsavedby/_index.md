---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_LastSavedBy metodo"
linktitle: "get_LastSavedBy"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Properties::BuiltInDocumentProperties::get_LastSavedBy. Ottiene o imposta il nome dell'ultimo autore in C++."
type: docs
weight: 16000
url: /it/cpp/aspose.words.properties/builtindocumentproperties/get_lastsavedby/
---
## BuiltInDocumentProperties::get_LastSavedBy method


Ottiene o imposta il nome dell'ultimo autore.

```cpp
System::String Aspose::Words::Properties::BuiltInDocumentProperties::get_LastSavedBy()
```

## Note


Aspose.Words non aggiorna questa proprietà.

## Esempi



Mostra come lavorare con le proprietà del documento nella categoria "Origin".
```cpp
// Apri un documento che abbiamo creato e modificato utilizzando Microsoft Word.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Properties.docx");
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();

// Le seguenti proprietà incorporate contengono informazioni relative alla creazione e alla modifica di questo documento.
// Possiamo fare clic con il tasto destro su questo documento in Esplora Risorse e trovare
// queste proprietà tramite "Properties" -> "Details" -> categoria "Origin".
// Campi come PRINTDATE e EDITTIME possono visualizzare questi valori nel corpo del documento.
std::cout << System::String::Format(u"Created using {0}, on {1}", properties->get_NameOfApplication(), properties->get_CreatedTime()) << std::endl;
std::cout << System::String::Format(u"Minutes spent editing: {0}", properties->get_TotalEditingTime()) << std::endl;
std::cout << System::String::Format(u"Date/time last printed: {0}", properties->get_LastPrinted()) << std::endl;
std::cout << System::String::Format(u"Template document: {0}", properties->get_Template()) << std::endl;

// Possiamo anche modificare i valori delle proprietà incorporate.
properties->set_Company(u"Doe Ltd.");
properties->set_Manager(u"Jane Doe");
properties->set_Version(5);
System::WithLambda::setter_post_increment_wrap(GETTER_SETTER_LAMBDA_ARGS(properties, RevisionNumber));

// Microsoft Word aggiorna automaticamente le seguenti proprietà quando salviamo il documento.
// Per utilizzare queste proprietà con Aspose.Words, dovremo impostare manualmente i valori.
properties->set_LastSavedBy(u"John Doe");
properties->set_LastSavedTime(System::DateTime::get_Now());

// Possiamo fare clic con il tasto destro su questo documento in Esplora Risorse e trovare queste proprietà in "Properties" -> "Details" -> "Origin".
doc->Save(get_ArtifactsDir() + u"DocumentProperties.Origin.docx");
```

## Vedi anche

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
