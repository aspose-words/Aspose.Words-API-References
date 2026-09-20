---
title: "Constructor ChmLoadOptions de Aspose::Words::Loading::ChmLoadOptions"
linktitle: "ChmLoadOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Constructor ChmLoadOptions de Aspose::Words::Loading::ChmLoadOptions. Inicializa una nueva instancia de esta clase con valores predeterminados en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.loading/chmloadoptions/chmloadoptions/
---
## ChmLoadOptions::ChmLoadOptions constructor


Inicializa una nueva instancia de esta clase con valores predeterminados.

```cpp
Aspose::Words::Loading::ChmLoadOptions::ChmLoadOptions()
```


## Ejemplos



Muestra cómo resolver URLs como "ms-its:myfile.chm::/index.htm".
```cpp
// Nuestro documento contiene URL como "ms-its:amhelp.chm::....htm", pero tiene un nombre diferente,
// por lo que los enlaces de archivo no funcionan después de guardarlo en HTML.
// Necesitamos definir el nombre de archivo original en 'ChmLoadOptions' para evitar este comportamiento.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::ChmLoadOptions>();
loadOptions->set_OriginalFileName(u"amhelp.chm");

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::IO::File::ReadAllBytes(get_MyDir() + u"Document with ms-its links.chm")), loadOptions);

doc->Save(get_ArtifactsDir() + u"ExChmLoadOptions.OriginalFileName.html");
```

## Ver también

* Class [ChmLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
