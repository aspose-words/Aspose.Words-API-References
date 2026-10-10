---
title: "Aspose::Words::FileFormatUtil::SaveFormatToExtension method"
linktitle: "SaveFormatToExtension"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::FileFormatUtil::SaveFormatToExtension method. Converte un valore enumerato di formato di salvataggio in un'estensione di file. L'estensione restituita è una stringa in minuscolo con un punto iniziale in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words/fileformatutil/saveformattoextension/
---
## FileFormatUtil::SaveFormatToExtension method


Converte un valore enumerato di formato di salvataggio in un'estensione di file. L'estensione restituita è una stringa in minuscolo con un punto iniziale.

```cpp
static System::String Aspose::Words::FileFormatUtil::SaveFormatToExtension(Aspose::Words::SaveFormat saveFormat)
```

## Note


Il valore [WordML](../../saveformat/) viene convertito in ".wml".

Il valore [FlatOpc](../../saveformat/) viene convertito in ".fopc".

## Esempi



Mostra come utilizzare i metodi [FileFormatUtil](../) per rilevare il formato di un documento.
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

* Enum [SaveFormat](../../saveformat/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
