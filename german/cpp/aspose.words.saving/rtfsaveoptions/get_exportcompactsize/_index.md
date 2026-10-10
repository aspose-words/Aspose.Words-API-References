---
title: "Aspose::Words::Saving::RtfSaveOptions::get_ExportCompactSize Methode"
linktitle: "get_ExportCompactSize"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::RtfSaveOptions::get_ExportCompactSize Methode. Ermöglicht es, die erzeugten RTF‑Dokumente kleiner zu machen, aber wenn sie RTL‑Text (right-to-left) enthalten, wird dieser nicht korrekt angezeigt. Der Standardwert ist false in C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words.saving/rtfsaveoptions/get_exportcompactsize/
---
## RtfSaveOptions::get_ExportCompactSize method


Ermöglicht, die Ausgabe‑RTF‑Dokumente kleiner zu machen, aber wenn sie RTL‑ (rechts‑nach‑links) Text enthalten, wird dieser nicht korrekt angezeigt. Standardwert ist **false**.

```cpp
bool Aspose::Words::Saving::RtfSaveOptions::get_ExportCompactSize() const
```

## Hinweise


Wenn das Dokument, das Sie mit Aspose.Words in RTF konvertieren möchten, keinen right-to-left‑Text in Sprachen wie Arabisch enthält, können Sie diese Option auf **true** setzen, um die Größe des resultierenden RTF zu reduzieren.

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
