---
title: "Método Aspose::Words::Saving::SvgSaveOptions::get_IdPrefix"
linktitle: "get_IdPrefix"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::SvgSaveOptions::get_IdPrefix. Especifica un prefijo que se antepone a todos los IDs de elementos generados en el documento de salida. El valor predeterminado es null y no se antepone ningún prefijo en C++."
type: docs
weight: 4250
url: /es/cpp/aspose.words.saving/svgsaveoptions/get_idprefix/
---
## SvgSaveOptions::get_IdPrefix method


Especifica un prefijo que se antepone a todos los IDs de elementos generados en el documento de salida. El valor predeterminado es null y no se antepone ningún prefijo.

```cpp
System::String Aspose::Words::Saving::SvgSaveOptions::get_IdPrefix() const
```


## Ejemplos



Muestra cómo agregar un prefijo que se antepone a todos los IDs de elementos generados (svg).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Id prefix.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_IdPrefix(u"pfx1_");

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.IdPrefixSvg.html", saveOptions);
```

## Ver también

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
