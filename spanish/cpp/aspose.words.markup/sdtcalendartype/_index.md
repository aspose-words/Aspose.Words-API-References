---
title: "Aspose::Words::Markup::SdtCalendarType enumeración"
linktitle: "SdtCalendarType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Markup::SdtCalendarType enumeración. Especifica los tipos posibles de calendarios que pueden usarse para especificar CalendarType en un documento Office Open XML en C++."
type: docs
weight: 19000
url: /es/cpp/aspose.words.markup/sdtcalendartype/
---
## SdtCalendarType enum


Especifica los tipos posibles de calendarios que pueden usarse para especificar [CalendarType](../structureddocumenttag/get_calendartype/) en un documento Office Open XML.

```cpp
enum class SdtCalendarType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Default | 0 | Usado como valor predeterminado en OOXML. Equivale a [Gregorian](./). |
| Gregorian | n/a | Especifica que se debe usar el calendario gregoriano, tal como se define en ISO 8601. Este calendario debe localizarse al idioma apropiado. |
| GregorianArabic | n/a | Especifica que se debe usar el calendario gregoriano, tal como se define en ISO 8601. Los valores de este calendario deben presentarse en árabe. |
| GregorianMeFrench | n/a | Especifica que se debe usar el calendario gregoriano, tal como se define en ISO 8601. Los valores de este calendario deben presentarse en francés del Oriente Medio. |
| GregorianUs | n/a | Especifica que se debe usar el calendario gregoriano, tal como se define en ISO 8601. Los valores de este calendario deben presentarse en inglés. |
| GregorianXlitEnglish | n/a | Especifica que se debe usar el calendario gregoriano, tal como se define en ISO 8601. Los valores de este calendario deben ser la representación de las cadenas en inglés en los caracteres árabes correspondientes (la transliteración al árabe de las cadenas en inglés para el calendario gregoriano). |
| GregorianXlitFrench | n/a | Especifica que se debe usar el calendario gregoriano, tal como se define en ISO 8601. Los valores de este calendario deben ser la representación de las cadenas en francés en los caracteres árabes correspondientes (la transliteración al árabe de las cadenas en francés para el calendario gregoriano). |
| Hebreo | n/a | Especifica que se debe usar el calendario lunar hebreo, según la fórmula de Gauss para la Pascua [CITATION] y The Complete Restatement of Oral Law (Mishneh Torah). |
| Hijri | n/a | Especifica que se debe usar el calendario lunar hijri, según el Reino de Arabia Saudita, Ministerio de Asuntos Islámicos, Endowments, Da‘wah y Guidance. |
| Japón | n/a | Especifica que se debe usar el calendario de la era del emperador japonés, según la Norma Industrial Japonesa JIS X 0301. |
| Corea | n/a | Especifica que se debe usar el calendario coreano de la Era Tangun, según lo descrito por la Ley Coreana No. 4. |
| None | n/a | Especifica que no se debe usar ningún calendario. |
| Saka | n/a | Especifica que se debe usar el calendario de la Era Saka, según lo descrito por el Comité de Reforma del Calendario de la India, como parte del Efemérides y Almanaque Náutico Indio. |
| Taiwán | n/a | Especifica que se debe usar el calendario taiwanés, según lo definido por la Norma Nacional China CNS 7648. |
| Tailandés | n/a | Especifica que se debe usar el calendario tailandés, según lo definido por el Decreto Real de Su Majestad el Rey Vajiravudh (Rama VI) en la Gaceta Real B. E. 2456 (1913 d.C.) y por el decreto del Primer Ministro Phibunsongkhram (1941 d.C.) para iniciar el año el 1 de enero del calendario gregoriano y mapear el año cero al año gregoriano 543 a.C., se debe usar. |


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
