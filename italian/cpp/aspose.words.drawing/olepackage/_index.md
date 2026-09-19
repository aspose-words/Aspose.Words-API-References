---
title: "Aspose::Words::Drawing::OlePackage classe"
linktitle: "OlePackage"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::OlePackage classe. Consente di accedere alle proprietà del pacchetto OLE. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words.drawing/olepackage/
---
## OlePackage class


Consente di accedere alle proprietà del pacchetto OLE. Per saperne di più, visita l'articolo di documentazione [Working with Ole Objects](https://docs.aspose.com/words/cpp/working-with-ole-objects/).

```cpp
class OlePackage : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_DisplayName](./get_displayname/)() const | Ottiene o imposta il nome visualizzato del pacchetto OLE. |
| [get_FileName](./get_filename/)() const | Ottiene o imposta il nome file del pacchetto OLE. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DisplayName](./set_displayname/)(System::String) | Impostatore per [Aspose::Words::Drawing::OlePackage::get_DisplayName](./get_displayname/). |
| [set_FileName](./set_filename/)(System::String) | Impostatore per [Aspose::Words::Drawing::OlePackage::get_FileName](./get_filename/). |
| static [Type](./type/)() |  |

## Esempi



Mostra come inserire un oggetto OLE in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Gli oggetti OLE ci consentono di aprire altri file nel file system locale usando un'altra applicazione installata
// nel nostro sistema operativo facendo doppio clic sulla forma che contiene l'oggetto OLE nel corpo del documento.
// In questo caso, il nostro file esterno sarà un archivio ZIP.
System::ArrayPtr<uint8_t> zipFileBytes = System::IO::File::ReadAllBytes(get_DatabaseDir() + u"cat001.zip");

{
    auto stream = System::MakeObject<System::IO::MemoryStream>(zipFileBytes);
    System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertOleObject(stream, u"Package", true, nullptr);

    shape->get_OleFormat()->get_OlePackage()->set_FileName(u"Package file name.zip");
    shape->get_OleFormat()->get_OlePackage()->set_DisplayName(u"Package display name.zip");
}

doc->Save(get_ArtifactsDir() + u"Shape.InsertOlePackage.docx");
```

## Vedi anche

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
