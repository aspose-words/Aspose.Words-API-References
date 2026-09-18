---
title: "Aspose::Words::Saving::RtfSaveOptions::get_ExportImagesForOldReaders Methode"
linktitle: "get_ExportImagesForOldReaders"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::RtfSaveOptions::get_ExportImagesForOldReaders Methode. Gibt an, ob die Schlüsselwörter für \"old readers\" in das RTF geschrieben werden oder nicht. Dies kann die Größe des RTF‑Dokuments erheblich beeinflussen. Der Standardwert ist true in C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words.saving/rtfsaveoptions/get_exportimagesforoldreaders/
---
## RtfSaveOptions::get_ExportImagesForOldReaders method


Gibt an, ob die Schlüsselwörter für „alte Leser“ in das RTF geschrieben werden oder nicht. Dies kann die Größe des RTF‑Dokuments erheblich beeinflussen. Standardwert ist **true**.

```cpp
bool Aspose::Words::Saving::RtfSaveOptions::get_ExportImagesForOldReaders() const
```

## Hinweise


"Old readers" sind Anwendungen vor Microsoft Word 97 und auch WordPad. Wenn diese Option **true** ist, schreibt Aspose.Words zusätzliche RTF‑Schlüsselwörter. Diese Schlüsselwörter ermöglichen, dass das Dokument korrekt angezeigt wird, wenn es in einer "old reader"‑Anwendung geöffnet wird, können jedoch die Dokumentgröße erheblich vergrößern.

Wenn Sie diese Option auf **false** setzen, werden nur Bilder in den Formaten WMF, EMF und BMP in "old readers" angezeigt.

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

* Class [RtfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
