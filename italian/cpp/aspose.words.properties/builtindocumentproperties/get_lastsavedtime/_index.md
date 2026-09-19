---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_LastSavedTime metodo"
linktitle: "get_LastSavedTime"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_LastSavedTime metodo. Ottiene o imposta l'ora dell'ultimo salvataggio in UTC in C++."
type: docs
weight: 17000
url: /it/cpp/aspose.words.properties/builtindocumentproperties/get_lastsavedtime/
---
## BuiltInDocumentProperties::get_LastSavedTime method


Ottiene o imposta l'ora dell'ultimo salvataggio in UTC.

```cpp
System::DateTime Aspose::Words::Properties::BuiltInDocumentProperties::get_LastSavedTime()
```

## Note


Per i documenti originati dal formato RTF, questa proprietà restituisce l'ora locale dell'ultima operazione di salvataggio.

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


Mostra come utilizzare il campo SAVEDATE per visualizzare data/ora dell'operazione di salvataggio più recente del documento eseguita con Microsoft Word.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->Writeln(u" Date this document was last saved:");

// Possiamo usare il campo SAVEDATE per visualizzare data e ora dell'ultima operazione di salvataggio sul documento.
// L'operazione di salvataggio a cui si riferiscono questi campi è il salvataggio manuale in un'applicazione come Microsoft Word,
// non il metodo Save del documento.
// Di seguito sono riportati tre diversi tipi di calendario in base ai quali il campo SAVEDATE può visualizzare data/ora.
// 1 -  Calendario lunare islamico:
builder->Write(u"According to the Lunar Calendar - ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseLunarCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\h", field->GetFieldCode());

// 2 -  Calendario Umm al-Qura:
builder->Write(u"\nAccording to the Umm al-Qura calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseUmAlQuraCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\u", field->GetFieldCode());

// 3 - Calendario nazionale indiano:
builder->Write(u"\nAccording to the Indian National calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseSakaEraCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\s", field->GetFieldCode());

// I campi SAVEDATE prendono i loro valori di data/ora dalla proprietà incorporata LastSavedTime.
// Il metodo Save del documento non aggiornerà questo valore, ma possiamo comunque aggiornarlo manualmente.
doc->get_BuiltInDocumentProperties()->set_LastSavedTime(System::DateTime::get_Now());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SAVEDATE.docx");
```

## Vedi anche

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
