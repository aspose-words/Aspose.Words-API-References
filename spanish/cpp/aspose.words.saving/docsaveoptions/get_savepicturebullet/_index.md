---
title: "Aspose::Words::Saving::DocSaveOptions::get_SavePictureBullet método"
linktitle: "get_SavePictureBullet"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::DocSaveOptions::get_SavePictureBullet método. Cuando es false, los datos de PictureBullet no se guardan en el documento de salida. El valor predeterminado es true en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.saving/docsaveoptions/get_savepicturebullet/
---
## DocSaveOptions::get_SavePictureBullet method


Cuando **false**, los datos de PictureBullet no se guardan en el documento de salida. El valor predeterminado es **true**.

```cpp
bool Aspose::Words::Saving::DocSaveOptions::get_SavePictureBullet() const
```

## Observaciones


Esta opción se proporciona para Word 97, que no puede trabajar correctamente con datos de PictureBullet. Para eliminar los datos de PictureBullet, establezca la opción a "false".

## Ejemplos



Muestra cómo omitir los datos de PictureBullet del documento al guardar.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Image bullet points.docx");

// Algunos procesadores de texto, como Microsoft Word 97, son incompatibles con los datos de PictureBullet.
// Al establecer una bandera en el objeto SaveOptions,
// podemos convertir todos los viñetas de imagen en viñetas ordinarias al guardar.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>(Aspose::Words::SaveFormat::Doc);
saveOptions->set_SavePictureBullet(false);

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.PictureBullets.doc", saveOptions);
```

## Ver también

* Class [DocSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
