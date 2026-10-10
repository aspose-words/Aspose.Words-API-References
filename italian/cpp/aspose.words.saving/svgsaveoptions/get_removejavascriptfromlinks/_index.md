---
title: "Metodo Aspose::Words::Saving::SvgSaveOptions::get_RemoveJavaScriptFromLinks"
linktitle: "get_RemoveJavaScriptFromLinks"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::SvgSaveOptions::get_RemoveJavaScriptFromLinks. Specifica se JavaScript verrà rimosso dai collegamenti. Il valore predefinito è false. Se questa opzione è abilitata, tutti i collegamenti contenenti JavaScript saranno sostituiti con \"javascript:void(0)\" in C++."
type: docs
weight: 4750
url: /it/cpp/aspose.words.saving/svgsaveoptions/get_removejavascriptfromlinks/
---
## SvgSaveOptions::get_RemoveJavaScriptFromLinks method


Specifica se JavaScript verrà rimosso dai collegamenti. Il valore predefinito è **false**. Se questa opzione è abilitata, tutti i collegamenti contenenti JavaScript saranno sostituiti con "javascript:void(0)".

```cpp
bool Aspose::Words::Saving::SvgSaveOptions::get_RemoveJavaScriptFromLinks() const
```


## Esempi



Mostra come rimuovere JavaScript dai collegamenti (svg).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"JavaScript in HREF.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_RemoveJavaScriptFromLinks(true);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.RemoveJavaScriptFromLinksSvg.html", saveOptions);
```

## Vedi anche

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
