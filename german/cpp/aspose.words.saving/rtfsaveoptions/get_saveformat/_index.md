---
title: "Aspose::Words::Saving::RtfSaveOptions::get_SaveFormat Methode"
linktitle: "get_SaveFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::RtfSaveOptions::get_SaveFormat Methode. Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses Save‑Options‑Objekt verwendet wird. Kann nur Rtf in C++ sein."
type: docs
weight: 5000
url: /de/cpp/aspose.words.saving/rtfsaveoptions/get_saveformat/
---
## RtfSaveOptions::get_SaveFormat method


Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses Save‑Options‑Objekt verwendet wird. Kann nur [Rtf](../../../aspose.words/saveformat/) sein.

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::RtfSaveOptions::get_SaveFormat() override
```


## Beispiele



Zeigt, wie man ein Dokument mit benutzerdefinierten Optionen als .rtf speichert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Erstellen Sie ein \"RtfSaveOptions\"‑Objekt, das an die \"Save\"‑Methode des Dokuments übergeben wird, um zu ändern, wie wir es als RTF speichern.
auto options = System::MakeObject<Aspose::Words::Saving::RtfSaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::Rtf, options->get_SaveFormat());

// Setzen Sie die Eigenschaft \"ExportCompactSize\" auf \"true\", um
// die Größe des gespeicherten Dokuments zu reduzieren, allerdings zulasten der Kompatibilität von Rechts‑nach‑Links‑Text.
options->set_ExportCompactSize(true);

// Setzen Sie die Eigenschaft \"ExportImagesFotOldReaders\" auf \"true\", um zusätzliche Schlüsselwörter zu verwenden, um sicherzustellen, dass unser Dokument ist
// kompatibel mit Lesern vor Microsoft Word 97 und WordPad ist.
// Setzen Sie die Eigenschaft \"ExportImagesFotOldReaders\" auf \"false\", um die Größe des Dokuments zu reduzieren,
// jedoch verhindern, dass alte Leser irgendwelche Nicht‑Metafile‑ oder BMP‑Bilder im Dokument lesen können.
options->set_ExportImagesForOldReaders(exportImagesForOldReaders);

doc->Save(get_ArtifactsDir() + u"RtfSaveOptions.ExportImages.rtf", options);
```

## Siehe auch

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [RtfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
