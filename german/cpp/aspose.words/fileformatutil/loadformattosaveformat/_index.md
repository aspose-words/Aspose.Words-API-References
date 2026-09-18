---
title: "Aspose::Words::FileFormatUtil::LoadFormatToSaveFormat Methode"
linktitle: "LoadFormatToSaveFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::FileFormatUtil::LoadFormatToSaveFormat Methode. Konvertiert einen LoadFormat-Wert in einen SaveFormat-Wert, falls möglich, in C++."
type: docs
weight: 7000
url: /de/cpp/aspose.words/fileformatutil/loadformattosaveformat/
---
## FileFormatUtil::LoadFormatToSaveFormat method


Konvertiert einen [LoadFormat](../../loadformat/)-Wert in einen [SaveFormat](../../saveformat/)-Wert, falls möglich.

```cpp
static Aspose::Words::SaveFormat Aspose::Words::FileFormatUtil::LoadFormatToSaveFormat(Aspose::Words::LoadFormat loadFormat)
```


## Beispiele



Zeigt, wie die [FileFormatUtil](../)-Methoden verwendet werden, um das Format eines Dokuments zu erkennen.
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

* Enum [SaveFormat](../../saveformat/)
* Enum [LoadFormat](../../loadformat/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
