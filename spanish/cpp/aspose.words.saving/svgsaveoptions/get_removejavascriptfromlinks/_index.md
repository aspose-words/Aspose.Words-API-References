---
title: "Aspose::Words::Saving::SvgSaveOptions::get_RemoveJavaScriptFromLinks method"
linktitle: "get_RemoveJavaScriptFromLinks"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::SvgSaveOptions::get_RemoveJavaScriptFromLinks method. Especifica si JavaScript será eliminado de los enlaces. El valor predeterminado es false. Si esta opción está habilitada, todos los enlaces que contengan JavaScript serán reemplazados por \"javascript:void(0)\" en C++."
type: docs
weight: 4750
url: /es/cpp/aspose.words.saving/svgsaveoptions/get_removejavascriptfromlinks/
---
## SvgSaveOptions::get_RemoveJavaScriptFromLinks method


Especifica si JavaScript será eliminado de los enlaces. El valor predeterminado es **false**. Si esta opción está habilitada, todos los enlaces que contengan JavaScript serán reemplazados por "javascript:void(0)".

```cpp
bool Aspose::Words::Saving::SvgSaveOptions::get_RemoveJavaScriptFromLinks() const
```


## Ejemplos



Muestra cómo eliminar JavaScript de los enlaces (svg).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"JavaScript in HREF.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_RemoveJavaScriptFromLinks(true);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.RemoveJavaScriptFromLinksSvg.html", saveOptions);
```

## Ver también

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
