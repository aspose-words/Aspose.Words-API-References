---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_IdPrefix Methode"
linktitle: "get_IdPrefix"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_IdPrefix Methode. Gibt ein Präfix an, das allen erzeugten Element‑IDs im Ausgabedokument vorangestellt wird. Der Standardwert ist null und es wird in C++ kein Präfix vorangestellt."
type: docs
weight: 10500
url: /de/cpp/aspose.words.saving/htmlfixedsaveoptions/get_idprefix/
---
## HtmlFixedSaveOptions::get_IdPrefix method


Gibt ein Präfix an, das allen erzeugten Element-IDs im Ausgabedokument vorangestellt wird. Standardwert ist null und es wird kein Präfix vorangestellt.

```cpp
System::String Aspose::Words::Saving::HtmlFixedSaveOptions::get_IdPrefix() const
```


## Beispiele



Zeigt, wie ein Präfix hinzugefügt wird, das allen erzeugten Element‑IDs vorangestellt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Id prefix.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
saveOptions->set_IdPrefix(u"pfx1_");

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.IdPrefix.html", saveOptions);
```

## Siehe auch

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
