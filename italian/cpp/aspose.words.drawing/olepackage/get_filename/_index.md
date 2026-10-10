---
title: "Metodo Aspose::Words::Drawing::OlePackage::get_FileName"
linktitle: "get_FileName"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::OlePackage::get_FileName method. Ottiene o imposta il nome file del pacchetto OLE in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.drawing/olepackage/get_filename/
---
## OlePackage::get_FileName method


Ottiene o imposta il nome file del pacchetto OLE.

```cpp
System::String Aspose::Words::Drawing::OlePackage::get_FileName() const
```


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

* Class [OlePackage](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
