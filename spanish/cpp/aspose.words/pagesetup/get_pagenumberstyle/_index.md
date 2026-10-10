---
title: "Aspose::Words::PageSetup::get_PageNumberStyle método"
linktitle: "get_PageNumberStyle"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::PageSetup::get_PageNumberStyle método. Obtiene o establece el formato del número de página en C++."
type: docs
weight: 34000
url: /es/cpp/aspose.words/pagesetup/get_pagenumberstyle/
---
## PageSetup::get_PageNumberStyle method


Obtiene o establece el formato del número de página.

```cpp
Aspose::Words::NumberStyle Aspose::Words::PageSetup::get_PageNumberStyle()
```


## Ejemplos



Muestra cómo configurar la numeración de páginas en una sección.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Section 1, page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 1, page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 1, page 3.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Writeln(u"Section 2, page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 2, page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 2, page 3.");

// Mueva el constructor de documentos al encabezado principal de la primera sección,
// que se mostrará en cada página de esa sección.
builder->MoveToSection(0);
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);

// Inserte un campo PAGE, que mostrará el número de la página actual.
builder->Write(u"Page ");
builder->InsertField(u"PAGE", u"");

// Configure la sección para que la cuenta de páginas que muestran los campos PAGE comience en 5.
// Además, configure todos los campos PAGE para que muestren sus números de página usando numerales romanos en mayúsculas.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_RestartPageNumbering(true);
pageSetup->set_PageStartingNumber(5);
pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);

// Cree otro encabezado principal para la segunda sección, con otro campo PAGE.
builder->MoveToSection(1);
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->Write(u" - ");
builder->InsertField(u"PAGE", u"");
builder->Write(u" - ");

// Configure la sección para que la cuenta de páginas que muestran los campos PAGE comience en 10.
// Además, configure todos los campos PAGE para que muestren sus números de página usando números arábigos.
pageSetup = doc->get_Sections()->idx_get(1)->get_PageSetup();
pageSetup->set_PageStartingNumber(10);
pageSetup->set_RestartPageNumbering(true);
pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::Arabic);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageNumbering.docx");
```

## Ver también

* Enum [NumberStyle](../../numberstyle/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
