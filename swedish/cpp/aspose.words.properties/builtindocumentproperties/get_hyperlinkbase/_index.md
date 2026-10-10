---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinkBase metod"
linktitle: "get_HyperlinkBase"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinkBase metod. Anger bassträngen som används för att utvärdera relativa hyperlänkar i detta dokument i C++."
type: docs
weight: 13000
url: /sv/cpp/aspose.words.properties/builtindocumentproperties/get_hyperlinkbase/
---
## BuiltInDocumentProperties::get_HyperlinkBase method


Anger bassträngen som används för att utvärdera relativa hyperlänkar i detta dokument.

```cpp
System::String Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinkBase()
```

## Anmärkningar


Aspose.Words använder inte den här egenskapen.

## Exempel



Visar hur man lagrar basdelen av en hyperlänk i dokumentets egenskaper.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga en relativ hyperlänk till ett dokument i det lokala filsystemet med namnet "Document.docx".
// Att klicka på länken i Microsoft Word kommer att öppna det angivna dokumentet, om det är tillgängligt.
builder->InsertHyperlink(u"Relative hyperlink", u"Document.docx", false);

// Den här länken är relativ. Om det inte finns någon "Document.docx" i samma mapp
// som dokumentet som innehåller länken, kommer länken att vara bruten.
ASSERT_FALSE(System::IO::File::Exists(get_ArtifactsDir() + u"Document.docx"));
doc->Save(get_ArtifactsDir() + u"DocumentProperties.HyperlinkBase.BrokenLink.docx");

// Dokumentet vi försöker länka till ligger i en annan katalog än den vi planerar att spara dokumentet i.
// Vi skulle kunna fixa länkar så här genom att lägga ett absolut filnamn i varje.
// Alternativt skulle vi kunna tillhandahålla en baslänk som varje hyperlänk med ett relativt filnamn
// kommer att läggas till i början av dess länk när vi klickar på den.
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();
properties->set_HyperlinkBase(get_MyDir());

ASSERT_TRUE(System::IO::File::Exists(properties->get_HyperlinkBase() + (System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(doc->get_Range()->get_Fields()->idx_get(0)))->get_Address()));

doc->Save(get_ArtifactsDir() + u"DocumentProperties.HyperlinkBase.WorkingLink.docx");
```

## Se även

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
