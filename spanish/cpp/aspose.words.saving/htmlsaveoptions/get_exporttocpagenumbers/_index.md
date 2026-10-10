---
title: "Método Aspose::Words::Saving::HtmlSaveOptions::get_ExportTocPageNumbers"
linktitle: "get_ExportTocPageNumbers"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::HtmlSaveOptions::get_ExportTocPageNumbers. Especifica si se deben escribir números de página en la tabla de contenido al guardar en HTML, MHTML y EPUB. El valor predeterminado es false en C++."
type: docs
weight: 29000
url: /es/cpp/aspose.words.saving/htmlsaveoptions/get_exporttocpagenumbers/
---
## HtmlSaveOptions::get_ExportTocPageNumbers method


Especifica si se escriben los números de página en la tabla de contenido al guardar en HTML, MHTML y EPUB. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportTocPageNumbers() const
```


## Ejemplos



Muestra cómo mostrar números de página al guardar un documento con una tabla de contenido en .html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserte una tabla de contenido y luego rellene el documento con párrafos formateados usando un "Heading"
// estilo que la tabla de contenido tomará como entradas. Cada entrada mostrará el párrafo de encabezado a la izquierda,
// y el número de página que contiene el encabezado a la derecha.
auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));

builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 1"));
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Entry 1");
builder->Writeln(u"Entry 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Entry 3");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Entry 4");
fieldToc->UpdatePageNumbers();
doc->UpdateFields();

// Los documentos HTML no tienen páginas. Si guardamos este documento en HTML,
// los números de página que muestra nuestra tabla de contenido no tendrán sentido.
// Al guardar el documento en HTML, podemos pasar un objeto SaveOptions para omitir estos números de página de la tabla de contenido.
// Si establecemos la bandera "ExportTocPageNumbers" en "true",
// cada entrada de la tabla de contenido mostrará el encabezado, el separador y el número de página, preservando su apariencia en Microsoft Word.
// Si establecemos la bandera "ExportTocPageNumbers" en "false",
// la operación de guardado omitirá tanto el separador como el número de página y dejará el encabezado de cada entrada intacto.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportTocPageNumbers(exportTocPageNumbers);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportTocPageNumbers.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportTocPageNumbers.html");

if (exportTocPageNumbers)
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<span>Entry 1</span>") + u"<span style=\"width:428.14pt; font-family:'Lucida Console'; font-size:10pt; display:inline-block; -aw-font-family:'Times New Roman'; " + u"-aw-tabstop-align:right; -aw-tabstop-leader:dots; -aw-tabstop-pos:469.8pt\">.......................................................................</span>" + u"<span>2</span>" + u"</p>"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<p style=\"margin-top:0pt; margin-bottom:0pt\">") + u"<span>Entry 2</span>" + u"</p>"));
}
```

## Ver también

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
