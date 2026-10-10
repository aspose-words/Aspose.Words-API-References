---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_RevisionNumber Methode"
linktitle: "get_RevisionNumber"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_RevisionNumber Methode. Gibt die Dokumentversionsnummer zurück oder setzt sie in C++."
type: docs
weight: 24000
url: /de/cpp/aspose.words.properties/builtindocumentproperties/get_revisionnumber/
---
## BuiltInDocumentProperties::get_RevisionNumber method


Liest oder setzt die Revisionsnummer des Dokuments.

```cpp
int32_t Aspose::Words::Properties::BuiltInDocumentProperties::get_RevisionNumber()
```

## Hinweise


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


Zeigt, wie man mit REVNUM-Feldern arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Current revision #");

// Fügen Sie ein REVNUM-Feld ein, das die aktuelle Revisionsnummer-Eigenschaft des Dokuments anzeigt.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldRevNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldRevisionNum, true));

ASSERT_EQ(u" REVNUM ", field->GetFieldCode());
ASSERT_EQ(u"1", field->get_Result());
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_RevisionNumber());

// Diese Eigenschaft zählt, wie oft ein Dokument in Microsoft Word gespeichert wurde,
// und ist nicht mit nachverfolgten Revisionen verbunden. Wir können es finden, indem wir im Windows Explorer mit der rechten Maustaste auf das Dokument klicken.
// über Eigenschaften -> Details. Wir können diese Eigenschaft manuell aktualisieren.
System::WithLambda::setter_post_increment_wrap(GETTER_SETTER_LVAL_LAMBDA_ARGS(doc->get_BuiltInDocumentProperties(), RevisionNumber));
field->Update();

ASSERT_EQ(u"2", field->get_Result());
```

## Siehe auch

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
