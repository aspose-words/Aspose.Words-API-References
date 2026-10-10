---
title: "Aspose::Words::Saving::DocSaveOptions::get_AlwaysCompressMetafiles Methode"
linktitle: "get_AlwaysCompressMetafiles"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::DocSaveOptions::get_AlwaysCompressMetafiles Methode. Wenn false, werden kleine Metadateien aus Leistungsgründen nicht komprimiert. Der Standardwert ist true, alle Metadateien werden unabhängig von ihrer Größe in C++ komprimiert."
type: docs
weight: 3000
url: /de/cpp/aspose.words.saving/docsaveoptions/get_alwayscompressmetafiles/
---
## DocSaveOptions::get_AlwaysCompressMetafiles method


Wenn **false**, werden kleine Metadateien aus Leistungsgründen nicht komprimiert. Der Standardwert ist **true**, alle Metadateien werden unabhängig von ihrer Größe komprimiert.

```cpp
bool Aspose::Words::Saving::DocSaveOptions::get_AlwaysCompressMetafiles() const
```


## Beispiele



Zeigt, wie die Komprimierung von Metadateien in einem Dokument beim Speichern geändert wird.
```cpp
// Öffnen Sie ein Dokument, das eine Microsoft Equation 3.0‑Formel enthält.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Microsoft equation object.docx");

// Wenn wir ein Dokument speichern, werden kleinere Metadateien aus Leistungsgründen nicht komprimiert.
// Wir können in einem SaveOptions‑Objekt ein Flag setzen, um beim Speichern jede Metadatei zu komprimieren.
// Einige Editoren wie LibreOffice können unkomprimierte Metadateien nicht lesen.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>();
saveOptions->set_AlwaysCompressMetafiles(compressAllMetafiles);

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.AlwaysCompressMetafiles.docx", saveOptions);
```

## Siehe auch

* Class [DocSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
