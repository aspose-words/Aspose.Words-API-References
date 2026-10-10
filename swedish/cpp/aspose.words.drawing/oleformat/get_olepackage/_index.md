---
title: "Aspose::Words::Drawing::OleFormat::get_OlePackage metod"
linktitle: "get_OlePackage"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::OleFormat::get_OlePackage metod. Tillhandahåller åtkomst till OlePackage om OLE-objektet är ett OLE-paket. Returnerar null annars i C++."
type: docs
weight: 9000
url: /sv/cpp/aspose.words.drawing/oleformat/get_olepackage/
---
## OleFormat::get_OlePackage method


Tillhandahåller åtkomst till [OlePackage](../../olepackage/) om OLE-objektet är ett OLE-paket. Returnerar **null** annars.

```cpp
System::SharedPtr<Aspose::Words::Drawing::OlePackage> Aspose::Words::Drawing::OleFormat::get_OlePackage()
```


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

* Class [OlePackage](../../olepackage/)
* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
