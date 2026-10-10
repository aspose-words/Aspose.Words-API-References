---
title: "Aspose::Words::Saving::ResourceSavingArgs class"
linktitle: "ResourceSavingArgs"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::ResourceSavingArgs class. Tillhandahåller data för ResourceSaving()-händelsen. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 27000
url: /sv/cpp/aspose.words.saving/resourcesavingargs/
---
## ResourceSavingArgs class


Tillhandahåller data för [ResourceSaving()](../iresourcesavingcallback/resourcesaving/) händelsen. För att lära dig mer, besök dokumentationsartikeln [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class ResourceSavingArgs : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_Document](./get_document/)() const | Hämtar dokumentobjektet som för närvarande sparas. |
| [get_KeepResourceStreamOpen](./get_keepresourcestreamopen/)() const | Anger om Aspose.Words ska hålla strömmen öppen eller stänga den efter att en resurs har sparats. |
| [get_ResourceFileName](./get_resourcefilename/)() const | Hämtar eller anger filnamnet (utan sökväg) där resursen kommer att sparas. |
| [get_ResourceFileUri](./get_resourcefileuri/)() const | Hämtar eller anger den uniforma resursidentifieraren (URI) som används för att referera till resursfilen från dokumentet. |
| [get_ResourceStream](./get_resourcestream/)() const | Tillåter att ange strömmen där resursen ska sparas. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_KeepResourceStreamOpen](./set_keepresourcestreamopen/)(bool) | Sättare för [Aspose::Words::Saving::ResourceSavingArgs::get_KeepResourceStreamOpen](./get_keepresourcestreamopen/). |
| [set_ResourceFileName](./set_resourcefilename/)(const System::String\&) | Sättare för [Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileName](./get_resourcefilename/). |
| [set_ResourceFileUri](./set_resourcefileuri/)(const System::String\&) | Sättare för [Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileUri](./get_resourcefileuri/). |
| [set_ResourceStream](./set_resourcestream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Sättare för [Aspose::Words::Saving::ResourceSavingArgs::get_ResourceStream](./get_resourcestream/). |
| [set_ResourceStream](./set_resourcestream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| static [Type](./type/)() |  |
## Anmärkningar


Som standard, när Aspose.Words sparar ett dokument till HTML med fast sida, SVG eller Markdown, sparar det varje resurs i en separat fil. Aspose.Words använder dokumentets filnamn och ett unikt nummer för att generera unika filnamn för varje resurs som hittas i dokumentet.

[ResourceSavingArgs](./) allows to redefine how resource file names are generated or to completely circumvent saving of resources into files by providing your own stream objects.

För att tillämpa din egen logik för att generera resursfilnamn, använd egenskapen [ResourceFileName](./get_resourcefilename/).

För att spara resurser i strömmar istället för filer, använd egenskapen [ResourceStream](./get_resourcestream/).
## Se även

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
