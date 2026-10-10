---
title: "Aspose::Words::Drawing::OlePackage Klasse"
linktitle: "OlePackage"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::OlePackage Klasse. Ermöglicht den Zugriff auf OLE-Paket-Eigenschaften. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 9000
url: /de/cpp/aspose.words.drawing/olepackage/
---
## OlePackage class


Ermöglicht den Zugriff auf OLE-Paket-Eigenschaften. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Ole Objects](https://docs.aspose.com/words/cpp/working-with-ole-objects/).

```cpp
class OlePackage : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_DisplayName](./get_displayname/)() const | Liest oder setzt den Anzeigenamen des OLE-Pakets. |
| [get_FileName](./get_filename/)() const | Liest oder setzt den Dateinamen des OLE-Pakets. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DisplayName](./set_displayname/)(System::String) | Setter für [Aspose::Words::Drawing::OlePackage::get_DisplayName](./get_displayname/). |
| [set_FileName](./set_filename/)(System::String) | Setter für [Aspose::Words::Drawing::OlePackage::get_FileName](./get_filename/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
