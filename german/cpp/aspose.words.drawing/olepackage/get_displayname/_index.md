---
title: "Aspose::Words::Drawing::OlePackage::get_DisplayName-Methode"
linktitle: "get_DisplayName"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::OlePackage::get_DisplayName-Methode. Ruft den Anzeigenamen des OLE-Pakets ab oder legt ihn fest in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.drawing/olepackage/get_displayname/
---
## OlePackage::get_DisplayName method


Liest oder setzt den Anzeigenamen des OLE-Pakets.

```cpp
System::String Aspose::Words::Drawing::OlePackage::get_DisplayName() const
```


## Beispiele



Zeigt, wie ein OLE-Objekt in ein Dokument eingefügt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// OLE-Objekte ermöglichen es uns, andere Dateien im lokalen Dateisystem mit einer anderen installierten Anwendung zu öffnen.
// in unserem Betriebssystem, indem man auf die Form doppelklickt, die das OLE-Objekt im Dokumentenkörper enthält.
// In diesem Fall wird unsere externe Datei ein ZIP-Archiv sein.
System::ArrayPtr<uint8_t> zipFileBytes = System::IO::File::ReadAllBytes(get_DatabaseDir() + u"cat001.zip");

{
    auto stream = System::MakeObject<System::IO::MemoryStream>(zipFileBytes);
    System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertOleObject(stream, u"Package", true, nullptr);

    shape->get_OleFormat()->get_OlePackage()->set_FileName(u"Package file name.zip");
    shape->get_OleFormat()->get_OlePackage()->set_DisplayName(u"Package display name.zip");
}

doc->Save(get_ArtifactsDir() + u"Shape.InsertOlePackage.docx");
```

## Siehe auch

* Class [OlePackage](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
