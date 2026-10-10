---
title: "Aspose::Words::Markup::SdtDateStorageFormat enum"
linktitle: "SdtDateStorageFormat"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Markup::SdtDateStorageFormat enum. Especifica cómo se almacena/recupera la fecha para un SDT de fecha cuando el SDT está vinculado a un nodo XML en el almacén de datos del documento''s en C++."
type: docs
weight: 20000
url: /es/cpp/aspose.words.markup/sdtdatestorageformat/
---
## SdtDateStorageFormat enum


Especifica cómo se almacena/recupera la fecha de un SDT de fecha cuando el SDT está vinculado a un nodo XML en el almacén de datos del documento.

```cpp
enum class SdtDateStorageFormat
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Fecha | 0 | El valor de fecha para un SDT de fecha se almacena como una fecha en el formato estándar de Fecha del esquema XML. |
| DateTime | 1 | El valor de fecha para un SDT de fecha se almacena como una fecha en el formato estándar de DateTime del esquema XML. |
| Text | 2 | El valor de fecha para un SDT de fecha se almacena como texto. |
| Default | n/a | Predeterminado a [DateTime](./) |


## Ejemplos



Muestra cómo solicitar al usuario que ingrese una fecha con una etiqueta de documento estructurado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Inserte una etiqueta de documento estructurado que solicite al usuario ingresar una fecha.
// En Microsoft Word, este elemento se conoce como "Date picker content control".
// Cuando hacemos clic en la flecha en el extremo derecho de esta etiqueta en Microsoft Word,
// veremos una ventana emergente en forma de un calendario clicable.
// Podemos usar esa ventana emergente para seleccionar una fecha que la etiqueta mostrará.
auto sdtDate = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Date, Aspose::Words::Markup::MarkupLevel::Inline);

// Muestra la fecha, según la configuración regional árabe de Arabia Saudita.
sdtDate->set_DateDisplayLocale(System::Globalization::CultureInfo::GetCultureInfo(u"ar-SA")->get_LCID());

// Establece el formato con el que se mostrará la fecha.
sdtDate->set_DateDisplayFormat(u"dd MMMM, yyyy");
sdtDate->set_DateStorageFormat(Aspose::Words::Markup::SdtDateStorageFormat::DateTime);

// Muestra la fecha según el calendario hijri.
sdtDate->set_CalendarType(Aspose::Words::Markup::SdtCalendarType::Hijri);

// Antes de que el usuario elija una fecha en Microsoft Word, la etiqueta mostrará el texto "Click here to enter a date.".
// Según el calendario de la etiqueta, establece la propiedad "FullDate" para que la etiqueta muestre una fecha predeterminada.
sdtDate->set_FullDate(System::DateTime(1440, 10, 20));

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertNode(sdtDate);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.Date.docx");
```

## Ver también

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
