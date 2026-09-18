---
title: "Aspose::Words::Loading::ChmLoadOptions::get_OriginalFileName-Methode"
linktitle: "get_OriginalFileName"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Loading::ChmLoadOptions::get_OriginalFileName-Methode. Der Name der CHM-Datei. Standardwert ist null in C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words.loading/chmloadoptions/get_originalfilename/
---
## ChmLoadOptions::get_OriginalFileName method


Der Name der CHM‑Datei. Der Standardwert ist **null**.

```cpp
System::String Aspose::Words::Loading::ChmLoadOptions::get_OriginalFileName() const
```

## Hinweise


CHM-Dokumente können Links enthalten, die dasselbe Dokument über den Dateinamen referenzieren. Aspose.Words unterstützt solche Links und verwendet normalerweise [OriginalFileName](../../../aspose.words/document/get_originalfilename/), um zu prüfen, ob die von einem Link referenzierte Datei die Datei ist, die geladen wird. Wird ein Dokument aus einem Stream geladen, sollte sein ursprünglicher Dateiname über diese Eigenschaft explizit angegeben werden, da er nicht automatisch ermittelt werden kann.

Wenn ein CHM-Dokument aus einer Datei geladen wird und für diese Eigenschaft ein nicht‑null Wert angegeben ist, hat dieser Wert Vorrang vor dem tatsächlichen Dateinamen, der in [OriginalFileName](../../../aspose.words/document/get_originalfilename/) gespeichert ist.

## Beispiele



Zeigt, wie URLs wie "ms-its:myfile.chm::/index.htm" aufgelöst werden können.
```cpp
// Unser Dokument enthält URLs wie "ms-its:amhelp.chm::....htm", hat jedoch einen anderen Namen,
// so funktionieren Dateiverknüpfungen nach dem Speichern als HTML nicht.
// Wir müssen den ursprünglichen Dateinamen in 'ChmLoadOptions' festlegen, um dieses Verhalten zu vermeiden.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::ChmLoadOptions>();
loadOptions->set_OriginalFileName(u"amhelp.chm");

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::IO::File::ReadAllBytes(get_MyDir() + u"Document with ms-its links.chm")), loadOptions);

doc->Save(get_ArtifactsDir() + u"ExChmLoadOptions.OriginalFileName.html");
```

## Siehe auch

* Class [ChmLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
