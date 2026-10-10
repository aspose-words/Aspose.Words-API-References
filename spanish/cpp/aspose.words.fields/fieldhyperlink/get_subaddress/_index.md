---
title: "Método Aspose::Words::Fields::FieldHyperlink::get_SubAddress"
linktitle: "get_SubAddress"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Fields::FieldHyperlink::get_SubAddress. Obtiene o establece una ubicación en el archivo, como un marcador, a la que este hipervínculo salta en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.fields/fieldhyperlink/get_subaddress/
---
## FieldHyperlink::get_SubAddress method


Obtiene o establece una ubicación en el archivo, como un marcador, a la que este hipervínculo salta.

```cpp
System::String Aspose::Words::Fields::FieldHyperlink::get_SubAddress()
```


## Ejemplos



Muestra cómo usar campos HYPERLINK para enlazar a documentos en el sistema de archivos local.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldHyperlink, true));

// Cuando hacemos clic en este campo HYPERLINK en Microsoft Word,
// abrirá el documento vinculado y luego colocará el cursor en el marcador especificado.
field->set_Address(get_MyDir() + u"Bookmarks.docx");
field->set_SubAddress(u"MyBookmark3");
field->set_ScreenTip(System::String(u"Open ") + field->get_Address() + u" on bookmark " + field->get_SubAddress() + u" in a new window");

builder->Writeln();

// Cuando hacemos clic en este campo HYPERLINK en Microsoft Word,
// abrirá el documento vinculado y se desplazará automáticamente hacia abajo hasta el iframe especificado.
field = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldHyperlink, true));
field->set_Address(get_MyDir() + u"Iframes.html");
field->set_ScreenTip(System::String(u"Open ") + field->get_Address());
field->set_Target(u"iframe_3");
field->set_OpenInNewWindow(true);
field->set_IsImageMap(false);

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.HYPERLINK.docx");
```

## Ver también

* Class [FieldHyperlink](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
