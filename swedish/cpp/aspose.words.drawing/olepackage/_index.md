---
title: "Aspose::Words::Drawing::OlePackage klass"
linktitle: "OlePackage"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::OlePackage klass. Tillåter åtkomst till OLE Package-egenskaper. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 9000
url: /sv/cpp/aspose.words.drawing/olepackage/
---
## OlePackage class


Tillåter åtkomst till OLE‑paketegenskaper. För att lära dig mer, besök dokumentationsartikeln [Working with Ole Objects](https://docs.aspose.com/words/cpp/working-with-ole-objects/).

```cpp
class OlePackage : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_DisplayName](./get_displayname/)() const | Hämtar eller anger OLE Package-visningsnamn. |
| [get_FileName](./get_filename/)() const | Hämtar eller anger OLE Package-filnamn. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DisplayName](./set_displayname/)(System::String) | Sättare för [Aspose::Words::Drawing::OlePackage::get_DisplayName](./get_displayname/). |
| [set_FileName](./set_filename/)(System::String) | Sättare för [Aspose::Words::Drawing::OlePackage::get_FileName](./get_filename/). |
| static [Type](./type/)() |  |

## Exempel



Visar hur man infogar ett OLE-objekt i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// OLE-objekt låter oss öppna andra filer i det lokala filsystemet med en annan installerad applikation
// i vårt operativsystem genom att dubbelklicka på formen som innehåller OLE-objektet i dokumentets kropp.
// I det här fallet kommer vår externa fil att vara ett ZIP-arkiv.
System::ArrayPtr<uint8_t> zipFileBytes = System::IO::File::ReadAllBytes(get_DatabaseDir() + u"cat001.zip");

{
    auto stream = System::MakeObject<System::IO::MemoryStream>(zipFileBytes);
    System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertOleObject(stream, u"Package", true, nullptr);

    shape->get_OleFormat()->get_OlePackage()->set_FileName(u"Package file name.zip");
    shape->get_OleFormat()->get_OlePackage()->set_DisplayName(u"Package display name.zip");
}

doc->Save(get_ArtifactsDir() + u"Shape.InsertOlePackage.docx");
```

## Se även

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
