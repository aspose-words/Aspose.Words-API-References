---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_RemoveJavaScriptFromLinks metodo"
linktitle: "get_RemoveJavaScriptFromLinks"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_RemoveJavaScriptFromLinks metodo. Specifica se JavaScript verrà rimosso dai collegamenti. Il valore predefinito è false in C++."
type: docs
weight: 13500
url: /it/cpp/aspose.words.saving/htmlfixedsaveoptions/get_removejavascriptfromlinks/
---
## HtmlFixedSaveOptions::get_RemoveJavaScriptFromLinks method


Specifica se JavaScript verrà rimosso dai collegamenti. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_RemoveJavaScriptFromLinks() const
```


## Esempi



Mostra come rimuovere JavaScript dai collegamenti per documenti HTML a pagina fissa.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"JavaScript in HREF.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
saveOptions->set_RemoveJavaScriptFromLinks(true);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.RemoveJavaScriptFromLinks.html", saveOptions);
```


Mostra come rimuovere JavaScript dai collegamenti.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"JavaScript in HREF.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_RemoveJavaScriptFromLinks(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.RemoveJavaScriptFromLinks.html", saveOptions);
```

## Vedi anche

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
