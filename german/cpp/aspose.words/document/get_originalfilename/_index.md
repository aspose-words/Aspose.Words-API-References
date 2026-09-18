---
title: "Aspose::Words::Document::get_OriginalFileName method"
linktitle: "get_OriginalFileName"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::get_OriginalFileName-Methode. Gibt den ursprünglichen Dateinamen des Dokuments in C++ zurück."
type: docs
weight: 40000
url: /de/cpp/aspose.words/document/get_originalfilename/
---
## Document::get_OriginalFileName method


Liest den ursprünglichen Dateinamen des Dokuments.

```cpp
System::String Aspose::Words::Document::get_OriginalFileName() const
```

## Hinweise


Gibt **null** zurück, wenn das Dokument aus einem Stream geladen oder leer erstellt wurde.

## Beispiele



Zeigt, wie Details des Ladevorgangs eines Dokuments abgerufen werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

ASSERT_EQ(get_MyDir() + u"Document.docx", doc->get_OriginalFileName());
ASSERT_EQ(Aspose::Words::LoadFormat::Docx, doc->get_OriginalLoadFormat());
```


Zeigt, wie die Methoden von [FileFormatUtil](../../fileformatutil/) verwendet werden, um das Format eines Dokuments zu erkennen.
```cpp
// Laden Sie ein Dokument aus einer Datei, der die Dateierweiterung fehlt, und erkennen Sie anschließend ihr Dateiformat.
{
    System::SharedPtr<System::IO::FileStream> docStream = System::IO::File::OpenRead(get_MyDir() + u"Word document with missing file extension");
    System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(docStream);
    Aspose::Words::LoadFormat loadFormat = info->get_LoadFormat();

    ASSERT_EQ(Aspose::Words::LoadFormat::Doc, loadFormat);

    // Nachfolgend sind zwei Methoden zum Konvertieren eines LoadFormat in das entsprechende SaveFormat aufgeführt.
    // 1 -  Erhalte die Dateierweiterungszeichenkette für das LoadFormat und erhalte dann das entsprechende SaveFormat aus dieser Zeichenkette:
    System::String fileExtension = Aspose::Words::FileFormatUtil::LoadFormatToExtension(loadFormat);
    Aspose::Words::SaveFormat saveFormat = Aspose::Words::FileFormatUtil::ExtensionToSaveFormat(fileExtension);

    // 2 -  Konvertiere das LoadFormat direkt zu seinem SaveFormat:
    saveFormat = Aspose::Words::FileFormatUtil::LoadFormatToSaveFormat(loadFormat);

    // Lade ein Dokument aus dem Stream und speichere es anschließend mit der automatisch erkannten Dateierweiterung.
    auto doc = System::MakeObject<Aspose::Words::Document>(docStream);

    ASSERT_EQ(u".doc", Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));

    doc->Save(get_ArtifactsDir() + u"File.SaveToDetectedFileFormat" + Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));
}
```

## Siehe auch

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
