---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_CreatedTime metod"
linktitle: "get_CreatedTime"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_CreatedTime metod. Hämtar eller anger datum för dokumentets skapande i UTC i C++."
type: docs
weight: 11000
url: /sv/cpp/aspose.words.properties/builtindocumentproperties/get_createdtime/
---
## BuiltInDocumentProperties::get_CreatedTime method


Hämtar eller anger datum för dokumentets skapande i UTC.

```cpp
System::DateTime Aspose::Words::Properties::BuiltInDocumentProperties::get_CreatedTime()
```

## Anmärkningar


För dokument som har sitt ursprung i RTF-format returnerar denna egenskap den lokala tiden på författarens maskin vid dokumentets skapande.

Aspose.Words uppdaterar inte denna egenskap.

## Exempel



Visar hur man arbetar med dokumentegenskaper i kategorin "Origin".
```cpp
// Öppna ett dokument som vi har skapat och redigerat med Microsoft Word.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Properties.docx");
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();

// Följande inbyggda egenskaper innehåller information om skapandet och redigeringen av detta dokument.
// Vi kan högerklicka på detta dokument i Windows Explorer och hitta
// dessa egenskaper via "Properties" -> "Details" -> "Origin"-kategorin.
// Fält som PRINTDATE och EDITTIME kan visa dessa värden i dokumentets brödtext.
std::cout << System::String::Format(u"Created using {0}, on {1}", properties->get_NameOfApplication(), properties->get_CreatedTime()) << std::endl;
std::cout << System::String::Format(u"Minutes spent editing: {0}", properties->get_TotalEditingTime()) << std::endl;
std::cout << System::String::Format(u"Date/time last printed: {0}", properties->get_LastPrinted()) << std::endl;
std::cout << System::String::Format(u"Template document: {0}", properties->get_Template()) << std::endl;

// Vi kan också ändra värdena för inbyggda egenskaper.
properties->set_Company(u"Doe Ltd.");
properties->set_Manager(u"Jane Doe");
properties->set_Version(5);
System::WithLambda::setter_post_increment_wrap(GETTER_SETTER_LAMBDA_ARGS(properties, RevisionNumber));

// Microsoft Word uppdaterar följande egenskaper automatiskt när vi sparar dokumentet.
// För att använda dessa egenskaper med Aspose.Words måste vi ange värden för dem manuellt.
properties->set_LastSavedBy(u"John Doe");
properties->set_LastSavedTime(System::DateTime::get_Now());

// Vi kan högerklicka på detta dokument i Windows Explorer och hitta dessa egenskaper i "Properties" -> "Details" -> "Origin".
doc->Save(get_ArtifactsDir() + u"DocumentProperties.Origin.docx");
```

## Se även

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
