---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Template Methode"
linktitle: "get_Template"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Template Methode. Ruft den informativen Namen der Dokumentvorlage ab oder legt ihn fest in C++."
type: docs
weight: 27000
url: /de/cpp/aspose.words.properties/builtindocumentproperties/get_template/
---
## BuiltInDocumentProperties::get_Template method


Liest oder setzt den informativen Namen der Dokumentvorlage.

```cpp
System::String Aspose::Words::Properties::BuiltInDocumentProperties::get_Template()
```

## Hinweise


In Microsoft Word dient diese Eigenschaft nur zu Informationszwecken und enthält normalerweise nur den Dateinamen der Vorlage ohne den Pfad.

Ein leerer String bedeutet, dass das Dokument an die Normalvorlage angehängt ist.

Um den tatsächlichen Namen der angehängten Vorlage zu erhalten oder festzulegen, verwenden Sie die [AttachedTemplate](../../../aspose.words/document/get_attachedtemplate/) Eigenschaft.

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
