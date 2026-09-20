---
title: "Aspose::Words::Section::ClearHeadersFooters method"
linktitle: "ClearHeadersFooters"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Section::ClearHeadersFooters method. Borra los encabezados y pies de página de esta sección en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words/section/clearheadersfooters/
---
## Section::ClearHeadersFooters() method


Borra los encabezados y pies de página de esta sección.

```cpp
void Aspose::Words::Section::ClearHeadersFooters()
```

## Observaciones


El texto de todos los encabezados y pies de página se borra, pero los objetos [HeaderFooter](../../headerfooter/) en sí no se eliminan.

Esto hace que los encabezados y pies de página de esta sección estén vinculados a los encabezados y pies de página de la sección anterior.

## Ejemplos



Muestra cómo borrar el contenido de todos los encabezados y pies de página en una sección.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_EQ(0, doc->get_FirstSection()->get_HeadersFooters()->get_Count());

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Writeln(u"This is the primary header.");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Writeln(u"This is the primary footer.");

ASSERT_EQ(2, doc->get_FirstSection()->get_HeadersFooters()->get_Count());

ASSERT_EQ(u"This is the primary header.", doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetText().Trim());
ASSERT_EQ(u"This is the primary footer.", doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetText().Trim());

// Vacía todos los encabezados y pies de página de esta sección de todo su contenido.
// Los encabezados y pies de página seguirán presentes, pero no tendrán nada que mostrar.
doc->get_FirstSection()->ClearHeadersFooters();

ASSERT_EQ(2, doc->get_FirstSection()->get_HeadersFooters()->get_Count());

ASSERT_EQ(System::String::Empty, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetText().Trim());
ASSERT_EQ(System::String::Empty, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetText().Trim());
```

## Ver también

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Section::ClearHeadersFooters(bool) method


Borra los encabezados y pies de página de esta sección.

```cpp
void Aspose::Words::Section::ClearHeadersFooters(bool preserveWatermarks)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| preserveWatermarks | bool | Verdadero si las marcas de agua no deben eliminarse. |
## Observaciones


El texto de todos los encabezados y pies de página se borra, pero los objetos [HeaderFooter](../../headerfooter/) en sí no se eliminan.

Esto hace que los encabezados y pies de página de esta sección estén vinculados a los encabezados y pies de página de la sección anterior.

## Ejemplos



Muestra cómo borrar el contenido del encabezado y pie de página con o sin una marca de agua.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Header and footer types.docx");

// Añade una marca de agua de texto simple.
doc->get_Watermark()->SetText(u"Aspose Watermark");

// Asegúrate de que los encabezados y pies de página tengan contenido.
System::SharedPtr<Aspose::Words::HeaderFooterCollection> headersFooters = doc->get_FirstSection()->get_HeadersFooters();
ASSERT_EQ(u"First header", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderFirst)->GetText().Trim());
ASSERT_EQ(u"Second header", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderEven)->GetText().Trim());
ASSERT_EQ(u"Third header", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetText().Trim());
ASSERT_EQ(u"First footer", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterFirst)->GetText().Trim());
ASSERT_EQ(u"Second footer", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterEven)->GetText().Trim());
ASSERT_EQ(u"Third footer", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetText().Trim());

// Elimina todo el contenido del encabezado y pie de página excepto las marcas de agua.
doc->get_FirstSection()->ClearHeadersFooters(true);

headersFooters = doc->get_FirstSection()->get_HeadersFooters();
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderFirst)->GetText().Trim());
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderEven)->GetText().Trim());
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetText().Trim());
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterFirst)->GetText().Trim());
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterEven)->GetText().Trim());
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetText().Trim());
ASSERT_EQ(Aspose::Words::WatermarkType::Text, doc->get_Watermark()->get_Type());

// Elimina todo el contenido del encabezado y pie de página, incluidas las marcas de agua.
doc->get_FirstSection()->ClearHeadersFooters(false);
ASSERT_EQ(Aspose::Words::WatermarkType::None, doc->get_Watermark()->get_Type());
```

## Ver también

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
