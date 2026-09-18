---
title: "Aspose::Words::Saving::SvgSaveOptions::get_IdPrefix Methode"
linktitle: "get_IdPrefix"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::SvgSaveOptions::get_IdPrefix Methode. Gibt ein Präfix an, das allen erzeugten Element-IDs im Ausgabedokument vorangestellt wird. Standardwert ist null und es wird kein Präfix in C++ vorangestellt."
type: docs
weight: 4250
url: /de/cpp/aspose.words.saving/svgsaveoptions/get_idprefix/
---
## SvgSaveOptions::get_IdPrefix method


Gibt ein Präfix an, das allen erzeugten Element-IDs im Ausgabedokument vorangestellt wird. Standardwert ist null und es wird kein Präfix vorangestellt.

```cpp
System::String Aspose::Words::Saving::SvgSaveOptions::get_IdPrefix() const
```


## Beispiele



Zeigt, wie ein Präfix hinzugefügt wird, das allen erzeugten Element-IDs (svg) vorangestellt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Id prefix.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_IdPrefix(u"pfx1_");

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.IdPrefixSvg.html", saveOptions);
```

## Siehe auch

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
