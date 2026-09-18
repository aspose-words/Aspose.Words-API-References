---
title: "Aspose::Words::Drawing::OleFormat::get_OlePackage-Methode"
linktitle: "get_OlePackage"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::OleFormat::get_OlePackage-Methode. Gibt Zugriff auf OlePackage, wenn das OLE-Objekt ein OLE-Paket ist. Gibt sonst null zurück in C++."
type: docs
weight: 9000
url: /de/cpp/aspose.words.drawing/oleformat/get_olepackage/
---
## OleFormat::get_OlePackage method


Gibt Zugriff auf [OlePackage](../../olepackage/), wenn das OLE-Objekt ein OLE-Paket ist. Gibt sonst **null** zurück.

```cpp
System::SharedPtr<Aspose::Words::Drawing::OlePackage> Aspose::Words::Drawing::OleFormat::get_OlePackage()
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

* Class [OlePackage](../../olepackage/)
* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
