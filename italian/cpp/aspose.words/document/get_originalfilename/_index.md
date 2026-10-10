---
title: "Aspose::Words::Document::get_OriginalFileName method"
linktitle: "get_OriginalFileName"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Document::get_OriginalFileName. Ottiene il nome file originale del documento in C++."
type: docs
weight: 40000
url: /it/cpp/aspose.words/document/get_originalfilename/
---
## Document::get_OriginalFileName method


Ottiene il nome file originale del documento.

```cpp
System::String Aspose::Words::Document::get_OriginalFileName() const
```

## Note


Restituisce **null** se il documento è stato caricato da uno stream o creato vuoto.

## Esempi



Mostra come recuperare i dettagli dell'operazione di caricamento di un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

ASSERT_EQ(get_MyDir() + u"Document.docx", doc->get_OriginalFileName());
ASSERT_EQ(Aspose::Words::LoadFormat::Docx, doc->get_OriginalLoadFormat());
```


Mostra come utilizzare i metodi di [FileFormatUtil](../../fileformatutil/) per rilevare il formato di un documento.
```cpp
// Carica un documento da un file a cui manca l'estensione e quindi rileva il suo formato file.
{
    System::SharedPtr<System::IO::FileStream> docStream = System::IO::File::OpenRead(get_MyDir() + u"Word document with missing file extension");
    System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(docStream);
    Aspose::Words::LoadFormat loadFormat = info->get_LoadFormat();

    ASSERT_EQ(Aspose::Words::LoadFormat::Doc, loadFormat);

    // Di seguito sono riportati due metodi per convertire un LoadFormat nel relativo SaveFormat.
    // 1 -  Ottieni la stringa dell'estensione file per il LoadFormat, quindi ottieni il SaveFormat corrispondente da quella stringa:
    System::String fileExtension = Aspose::Words::FileFormatUtil::LoadFormatToExtension(loadFormat);
    Aspose::Words::SaveFormat saveFormat = Aspose::Words::FileFormatUtil::ExtensionToSaveFormat(fileExtension);

    // 2 -  Converti direttamente il LoadFormat nel suo SaveFormat:
    saveFormat = Aspose::Words::FileFormatUtil::LoadFormatToSaveFormat(loadFormat);

    // Carica un documento dallo stream e poi salvalo con l'estensione file rilevata automaticamente.
    auto doc = System::MakeObject<Aspose::Words::Document>(docStream);

    ASSERT_EQ(u".doc", Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));

    doc->Save(get_ArtifactsDir() + u"File.SaveToDetectedFileFormat" + Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));
}
```

## Vedi anche

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
