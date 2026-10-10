---
title: "Método Aspose::Words::StyleCollection::ClearQuickStyleGallery"
linktitle: "ClearQuickStyleGallery"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::StyleCollection::ClearQuickStyleGallery. Elimina todos los estilos del panel Quick Style Gallery en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words/stylecollection/clearquickstylegallery/
---
## StyleCollection::ClearQuickStyleGallery method


Elimina todos los estilos del panel Quick [Style](../../style/) Gallery.

```cpp
void Aspose::Words::StyleCollection::ClearQuickStyleGallery()
```


## Ejemplos



Muestra cómo eliminar estilos del panel [Style](../../style/) Gallery.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
// Nota: la eliminación de estilos funciona solo con el formato DOCX por ahora.
doc->get_Styles()->ClearQuickStyleGallery();

doc->Save(get_ArtifactsDir() + u"Styles.RemoveStylesFromStyleGallery.docx");
```

## Ver también

* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
