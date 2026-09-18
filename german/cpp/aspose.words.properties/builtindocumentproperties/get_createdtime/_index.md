---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_CreatedTime Methode"
linktitle: "get_CreatedTime"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_CreatedTime Methode. Ruft das Erstellungsdatum des Dokuments in UTC ab oder legt es fest in C++."
type: docs
weight: 11000
url: /de/cpp/aspose.words.properties/builtindocumentproperties/get_createdtime/
---
## BuiltInDocumentProperties::get_CreatedTime method


Liest oder setzt das Erstellungsdatum des Dokuments in UTC.

```cpp
System::DateTime Aspose::Words::Properties::BuiltInDocumentProperties::get_CreatedTime()
```

## Hinweise


Für Dokumente, die aus dem RTF-Format stammen, gibt diese Eigenschaft die lokale Zeit des Rechners des Autors zum Zeitpunkt der Dokumenterstellung zurück.

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

## Siehe auch

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
