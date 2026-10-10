---
title: "Método Aspose::Words::Saving::HtmlFixedSaveOptions::get_IdPrefix"
linktitle: "get_IdPrefix"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::HtmlFixedSaveOptions::get_IdPrefix. Especifica un prefijo que se antepone a todos los IDs de elementos generados en el documento de salida. El valor predeterminado es null y no se antepone ningún prefijo en C++."
type: docs
weight: 10500
url: /es/cpp/aspose.words.saving/htmlfixedsaveoptions/get_idprefix/
---
## HtmlFixedSaveOptions::get_IdPrefix method


Especifica un prefijo que se antepone a todos los IDs de elementos generados en el documento de salida. El valor predeterminado es null y no se antepone ningún prefijo.

```cpp
System::String Aspose::Words::Saving::HtmlFixedSaveOptions::get_IdPrefix() const
```


## Ejemplos



Muestra cómo agregar un prefijo que se antepone a todos los IDs de elementos generados.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Id prefix.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
saveOptions->set_IdPrefix(u"pfx1_");

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.IdPrefix.html", saveOptions);
```

## Ver también

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
