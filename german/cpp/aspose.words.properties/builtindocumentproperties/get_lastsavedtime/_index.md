---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_LastSavedTime Methode"
linktitle: "get_LastSavedTime"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_LastSavedTime Methode. Ruft den Zeitpunkt der letzten Speicherung in UTC ab oder legt ihn fest in C++."
type: docs
weight: 17000
url: /de/cpp/aspose.words.properties/builtindocumentproperties/get_lastsavedtime/
---
## BuiltInDocumentProperties::get_LastSavedTime method


Liest oder setzt die Zeit der letzten Speicherung in UTC.

```cpp
System::DateTime Aspose::Words::Properties::BuiltInDocumentProperties::get_LastSavedTime()
```

## Hinweise


Für Dokumente, die aus dem RTF-Format stammen, gibt diese Eigenschaft die lokale Zeit der letzten Speicheroperation zurück.

Aspose.Words aktualisiert diese Eigenschaft nicht.

## Beispiele



Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Origin" arbeitet.
```cpp
// Öffnen Sie ein Dokument, das wir mit Microsoft Word erstellt und bearbeitet haben.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Properties.docx");
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();

// Die folgenden integrierten Eigenschaften enthalten Informationen über die Erstellung und Bearbeitung dieses Dokuments.
// Wir können dieses Dokument im Windows Explorer mit der rechten Maustaste anklicken und finden
// diese Eigenschaften über "Properties" -> "Details" -> "Origin"‑Kategorie.
// Felder wie PRINTDATE und EDITTIME können diese Werte im Dokumentkörper anzeigen.
std::cout << System::String::Format(u"Created using {0}, on {1}", properties->get_NameOfApplication(), properties->get_CreatedTime()) << std::endl;
std::cout << System::String::Format(u"Minutes spent editing: {0}", properties->get_TotalEditingTime()) << std::endl;
std::cout << System::String::Format(u"Date/time last printed: {0}", properties->get_LastPrinted()) << std::endl;
std::cout << System::String::Format(u"Template document: {0}", properties->get_Template()) << std::endl;

// Wir können auch die Werte der integrierten Eigenschaften ändern.
properties->set_Company(u"Doe Ltd.");
properties->set_Manager(u"Jane Doe");
properties->set_Version(5);
System::WithLambda::setter_post_increment_wrap(GETTER_SETTER_LAMBDA_ARGS(properties, RevisionNumber));

// Microsoft Word aktualisiert die folgenden Eigenschaften automatisch, wenn wir das Dokument speichern.
// Um diese Eigenschaften mit Aspose.Words zu verwenden, müssen wir die Werte manuell festlegen.
properties->set_LastSavedBy(u"John Doe");
properties->set_LastSavedTime(System::DateTime::get_Now());

// Wir können dieses Dokument im Windows Explorer mit der rechten Maustaste anklicken und diese Eigenschaften unter "Eigenschaften" -> "Details" -> "Ursprung" finden.
doc->Save(get_ArtifactsDir() + u"DocumentProperties.Origin.docx");
```


Zeigt, wie das SAVEDATE‑Feld verwendet wird, um das Datum/Uhrzeit der zuletzt in Microsoft Word durchgeführten Speicheroperation des Dokuments anzuzeigen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->Writeln(u" Date this document was last saved:");

// Wir können das SAVEDATE‑Feld verwenden, um das Datum und die Uhrzeit der letzten Speicheroperation im Dokument anzuzeigen.
// Die Speicheroperation, auf die sich diese Felder beziehen, ist das manuelle Speichern in einer Anwendung wie Microsoft Word,
// nicht die Save‑Methode des Dokuments.
// Im Folgenden sind drei verschiedene Kalendertypen aufgeführt, nach denen das SAVEDATE‑Feld Datum/Uhrzeit anzeigen kann.
// 1 -  Islamischer Mondkalender:
builder->Write(u"According to the Lunar Calendar - ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseLunarCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\h", field->GetFieldCode());

// 2 -  Umm al‑Qura‑Kalender:
builder->Write(u"\nAccording to the Umm al-Qura calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseUmAlQuraCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\u", field->GetFieldCode());

// 3 -  Indischer Nationalkalender:
builder->Write(u"\nAccording to the Indian National calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseSakaEraCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\s", field->GetFieldCode());

// Die SAVEDATE‑Felder beziehen ihre Datums-/Uhrzeitwerte aus der integrierten Eigenschaft LastSavedTime.
// Die Save‑Methode des Dokuments aktualisiert diesen Wert nicht, aber wir können ihn dennoch manuell aktualisieren.
doc->get_BuiltInDocumentProperties()->set_LastSavedTime(System::DateTime::get_Now());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SAVEDATE.docx");
```

## Siehe auch

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
