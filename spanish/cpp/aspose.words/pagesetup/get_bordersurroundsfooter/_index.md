---
title: "Método Aspose::Words::PageSetup::get_BorderSurroundsFooter"
linktitle: "get_BorderSurroundsFooter"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::PageSetup::get_BorderSurroundsFooter. Especifica si el borde de la página incluye o excluye el pie de página en C++."
type: docs
weight: 8000
url: /es/cpp/aspose.words/pagesetup/get_bordersurroundsfooter/
---
## PageSetup::get_BorderSurroundsFooter method


Especifica si el borde de página incluye o excluye el pie de página.

```cpp
bool Aspose::Words::PageSetup::get_BorderSurroundsFooter()
```


## Ejemplos



Muestra cómo aplicar un borde a la página y al encabezado/pie de página.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world! This is the main body text.");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Write(u"This is the header.");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Write(u"This is the footer.");
builder->MoveToDocumentEnd();

// Inserte un borde azul de doble línea.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Double);
pageSetup->get_Borders()->set_Color(System::Drawing::Color::get_Blue());

// El objeto PageSetup de una sección tiene banderas "BorderSurroundsHeader" y "BorderSurroundsFooter" que determinan
// si un borde de página rodea el texto principal del cuerpo, también incluye el encabezado o el pie de página, respectivamente.
// Establezca la bandera "BorderSurroundsHeader" a "true" para rodear el encabezado con nuestro borde,
// y luego establezca la bandera "BorderSurroundsFooter" para dejar el pie de página fuera del borde.
pageSetup->set_BorderSurroundsHeader(true);
pageSetup->set_BorderSurroundsFooter(false);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageBorder.docx");
```

## Ver también

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
