---
title: "Aspose::Words::PageSetup::get_OddAndEvenPagesHeaderFooter método"
linktitle: "get_OddAndEvenPagesHeaderFooter"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::PageSetup::get_OddAndEvenPagesHeaderFooter método. Verdadero si el documento tiene encabezados y pies de página diferentes para las páginas impares y pares en C++."
type: docs
weight: 30000
url: /es/cpp/aspose.words/pagesetup/get_oddandevenpagesheaderfooter/
---
## PageSetup::get_OddAndEvenPagesHeaderFooter method


Verdadero si el documento tiene encabezados y pies de página diferentes para páginas impares y pares.

```cpp
bool Aspose::Words::PageSetup::get_OddAndEvenPagesHeaderFooter() const
```


## Ejemplos



Muestra cómo habilitar o deshabilitar los encabezados/pies de página pares.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// A continuación se presentan dos tipos de encabezados/pies de página.
// 1 -  El encabezado/pie de página "Primary", que aparece en cada página de la sección.
// Podemos sobrescribir el encabezado/pie de página principal con un encabezado/pie de página de primera y uno de página par.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Writeln(u"Primary header.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Writeln(u"Primary footer.");

// 2 -  El encabezado/pie de página "Even", que aparece en cada página par de esta sección.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderEven);
builder->Writeln(u"Even page header.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterEven);
builder->Writeln(u"Even page footer.");

builder->MoveToSection(0);
builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Cada sección tiene un objeto "PageSetup" que especifica propiedades relacionadas con la apariencia de la página
// como la orientación, el tamaño y los bordes.
// Establezca la propiedad "OddAndEvenPagesHeaderFooter" a "true"
// para mostrar el encabezado/pie de página par en las páginas pares.
// Establezca la propiedad "OddAndEvenPagesHeaderFooter" a "false"
// para mostrar el encabezado/pie de página principal en las páginas pares.
builder->get_PageSetup()->set_OddAndEvenPagesHeaderFooter(oddAndEvenPagesHeaderFooter);

doc->Save(get_ArtifactsDir() + u"PageSetup.OddAndEvenPagesHeaderFooter.docx");
```

## Ver también

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
