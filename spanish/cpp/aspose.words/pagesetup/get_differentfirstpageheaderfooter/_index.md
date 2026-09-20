---
title: "Aspose::Words::PageSetup::get_DifferentFirstPageHeaderFooter método"
linktitle: "get_DifferentFirstPageHeaderFooter"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::PageSetup::get_DifferentFirstPageHeaderFooter método. Verdadero si se utiliza un encabezado o pie de página diferente en la primera página en C++."
type: docs
weight: 13000
url: /es/cpp/aspose.words/pagesetup/get_differentfirstpageheaderfooter/
---
## PageSetup::get_DifferentFirstPageHeaderFooter method


Verdadero si se usa un encabezado o pie de página diferente en la primera página.

```cpp
bool Aspose::Words::PageSetup::get_DifferentFirstPageHeaderFooter()
```


## Ejemplos



Muestra cómo habilitar o deshabilitar los encabezados/pies de página principales.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// A continuación se presentan dos tipos de encabezados/pies de página.
// 1 -  El encabezado/pie de página "First", que aparece en la primera página de la sección.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderFirst);
builder->Writeln(u"First page header.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterFirst);
builder->Writeln(u"First page footer.");

// 2 -  El encabezado/pie de página "Primary", que aparece en cada página de la sección.
// Podemos sobrescribir el encabezado/pie de página principal con un encabezado/pie de página de primera y uno de página par.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Writeln(u"Primary header.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Writeln(u"Primary footer.");

builder->MoveToSection(0);
builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Cada sección tiene un objeto "PageSetup" que especifica propiedades relacionadas con la apariencia de la página
// como la orientación, el tamaño y los bordes.
// Establezca la propiedad "DifferentFirstPageHeaderFooter" en "true" para aplicar el primer encabezado/pie de página a la primera página.
// Establezca la propiedad "DifferentFirstPageHeaderFooter" en "false"
// para que la primera página muestre el encabezado/pie de página principal.
builder->get_PageSetup()->set_DifferentFirstPageHeaderFooter(differentFirstPageHeaderFooter);

doc->Save(get_ArtifactsDir() + u"PageSetup.DifferentFirstPageHeaderFooter.docx");
```

## Ver también

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
