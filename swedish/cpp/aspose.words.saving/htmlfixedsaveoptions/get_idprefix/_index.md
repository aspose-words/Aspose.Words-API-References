---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_IdPrefix metod"
linktitle: "get_IdPrefix"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_IdPrefix metod. Anger ett prefix som läggs till i början av alla genererade element‑ID:n i utdokumentet. Standardvärdet är null och inget prefix läggs till i C++."
type: docs
weight: 10500
url: /sv/cpp/aspose.words.saving/htmlfixedsaveoptions/get_idprefix/
---
## HtmlFixedSaveOptions::get_IdPrefix method


Anger ett prefix som läggs före alla genererade element-ID:n i utmatningsdokumentet. Standardvärdet är null och inget prefix läggs till.

```cpp
System::String Aspose::Words::Saving::HtmlFixedSaveOptions::get_IdPrefix() const
```


## Exempel



Visar hur man lägger till ett prefix som läggs till i början av alla genererade element‑ID:n.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Id prefix.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
saveOptions->set_IdPrefix(u"pfx1_");

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.IdPrefix.html", saveOptions);
```

## Se även

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
