---
title: "Método Aspose::Words::Saving::DocSaveOptions::get_AlwaysCompressMetafiles"
linktitle: "get_AlwaysCompressMetafiles"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::DocSaveOptions::get_AlwaysCompressMetafiles. Cuando es false, los metafiles pequeños no se comprimen por razones de rendimiento. El valor predeterminado es true, todos los metafiles se comprimen sin importar su tamaño en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.saving/docsaveoptions/get_alwayscompressmetafiles/
---
## DocSaveOptions::get_AlwaysCompressMetafiles method


Cuando **false**, los metafiles pequeños no se comprimen por razones de rendimiento. El valor predeterminado es **true**, todos los metafiles se comprimen sin importar su tamaño.

```cpp
bool Aspose::Words::Saving::DocSaveOptions::get_AlwaysCompressMetafiles() const
```


## Ejemplos



Muestra cómo cambiar la compresión de metafiles en un documento al guardarlo.
```cpp
// Abra un documento que contenga una fórmula Microsoft Equation 3.0.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Microsoft equation object.docx");

// Al guardar un documento, los metafiles más pequeños no se comprimen por razones de rendimiento.
// Podemos establecer una bandera en un objeto SaveOptions para comprimir cada metafile al guardar.
// Algunos editores, como LibreOffice, no pueden leer metafiles sin comprimir.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>();
saveOptions->set_AlwaysCompressMetafiles(compressAllMetafiles);

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.AlwaysCompressMetafiles.docx", saveOptions);
```

## Ver también

* Class [DocSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
