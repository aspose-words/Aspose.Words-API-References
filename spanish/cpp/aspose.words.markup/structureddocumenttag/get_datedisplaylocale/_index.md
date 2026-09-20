---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_DateDisplayLocale method"
linktitle: "get_DateDisplayLocale"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_DateDisplayLocale method. Permite establecer/obtener el formato de idioma para la fecha mostrada en este SDT en C++."
type: docs
weight: 13000
url: /es/cpp/aspose.words.markup/structureddocumenttag/get_datedisplaylocale/
---
## StructuredDocumentTag::get_DateDisplayLocale method


Permite establecer/obtener el formato de idioma para la fecha mostrada en este **SDT**.

```cpp
int32_t Aspose::Words::Markup::StructuredDocumentTag::get_DateDisplayLocale()
```

## Observaciones


Acceder a esta propiedad solo funcionará para el tipo de SDT [Date](../../sdttype/).

Para todos los demás tipos de SDT se producirá una excepción.

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

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
