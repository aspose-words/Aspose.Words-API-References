---
title: "Aspose::Words::Saving::OoxmlSaveOptions::get_KeepLegacyControlChars método"
linktitle: "get_KeepLegacyControlChars"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::OoxmlSaveOptions::get_KeepLegacyControlChars método. Conserva la representación original de los caracteres de control heredados en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.saving/ooxmlsaveoptions/get_keeplegacycontrolchars/
---
## OoxmlSaveOptions::get_KeepLegacyControlChars method


Mantiene la representación original de los caracteres de control heredados.

```cpp
bool Aspose::Words::Saving::OoxmlSaveOptions::get_KeepLegacyControlChars() const
```


## Ejemplos



Muestra cómo admitir caracteres de control heredados al convertir a .docx.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Legacy control character.doc");

// Cuando guardamos el documento en un formato OOXML, podemos crear un objeto OoxmlSaveOptions
// y luego pasarlo al método de guardado del documento para modificar cómo guardamos el documento.
// Establezca la propiedad "KeepLegacyControlChars" a "true" para preservar
// el carácter heredado "ShortDateTime" al guardar.
// Establezca la propiedad "KeepLegacyControlChars" a "false" para eliminar
// el carácter heredado "ShortDateTime" del documento de salida.
auto so = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
so->set_KeepLegacyControlChars(keepLegacyControlChars);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.KeepLegacyControlChars.docx", so);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.KeepLegacyControlChars.docx");

ASSERT_EQ(keepLegacyControlChars ? System::String(u"\u0013date \\@ \"MM/dd/yyyy\"\u0014\u0015\f") : System::String(u"\u001e\f"), doc->get_FirstSection()->get_Body()->GetText());
```

## Ver también

* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
