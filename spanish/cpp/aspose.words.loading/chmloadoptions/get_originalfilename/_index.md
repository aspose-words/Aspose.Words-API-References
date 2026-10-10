---
title: "Método get_OriginalFileName de Aspose::Words::Loading::ChmLoadOptions"
linktitle: "get_OriginalFileName"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método get_OriginalFileName de Aspose::Words::Loading::ChmLoadOptions. El nombre del archivo CHM. El valor predeterminado es null en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.loading/chmloadoptions/get_originalfilename/
---
## ChmLoadOptions::get_OriginalFileName method


El nombre del archivo CHM. El valor predeterminado es **null**.

```cpp
System::String Aspose::Words::Loading::ChmLoadOptions::get_OriginalFileName() const
```

## Observaciones


Los documentos CHM pueden contener enlaces que hacen referencia al mismo documento por nombre de archivo. Aspose.Words admite dichos enlaces y normalmente utiliza [OriginalFileName](../../../aspose.words/document/get_originalfilename/) para comprobar si el archivo referenciado por un enlace es el archivo que se está cargando. Si un documento se carga desde un flujo, su nombre de archivo original debe especificarse explícitamente mediante esta propiedad, ya que no puede determinarse automáticamente.

Si un documento CHM se carga desde un archivo y se especifica un valor no nulo para esta propiedad, el valor tendrá prioridad sobre el nombre real del archivo almacenado en [OriginalFileName](../../../aspose.words/document/get_originalfilename/).

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
