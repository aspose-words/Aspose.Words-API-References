---
title: "Aspose::Words::Loading::ChmLoadOptions::ChmLoadOptions Konstruktor"
linktitle: "ChmLoadOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Loading::ChmLoadOptions::ChmLoadOptions Konstruktor. Initialisiert eine neue Instanz dieser Klasse mit Standardwerten in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.loading/chmloadoptions/chmloadoptions/
---
## ChmLoadOptions::ChmLoadOptions constructor


Initialisiert eine neue Instanz dieser Klasse mit Standardwerten.

```cpp
Aspose::Words::Loading::ChmLoadOptions::ChmLoadOptions()
```


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
