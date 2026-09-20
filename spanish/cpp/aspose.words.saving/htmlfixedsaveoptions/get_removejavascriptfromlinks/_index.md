---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_RemoveJavaScriptFromLinks método"
linktitle: "get_RemoveJavaScriptFromLinks"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_RemoveJavaScriptFromLinks método. Especifica si JavaScript será eliminado de los enlaces. El valor predeterminado es false en C++."
type: docs
weight: 13500
url: /es/cpp/aspose.words.saving/htmlfixedsaveoptions/get_removejavascriptfromlinks/
---
## HtmlFixedSaveOptions::get_RemoveJavaScriptFromLinks method


Especifica si JavaScript será eliminado de los enlaces. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_RemoveJavaScriptFromLinks() const
```


## Ejemplos



Muestra cómo eliminar JavaScript de los enlaces para documentos HTML de página fija.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"JavaScript in HREF.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
saveOptions->set_RemoveJavaScriptFromLinks(true);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.RemoveJavaScriptFromLinks.html", saveOptions);
```


Muestra cómo eliminar JavaScript de los enlaces.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"JavaScript in HREF.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_RemoveJavaScriptFromLinks(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.RemoveJavaScriptFromLinks.html", saveOptions);
```

## Ver también

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
