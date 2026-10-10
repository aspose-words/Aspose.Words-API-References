---
title: "Método Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitHeadingLevel"
linktitle: "get_DocumentSplitHeadingLevel"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitHeadingLevel. Especifica el nivel máximo de encabezados en el que dividir el documento. El valor predeterminado es %2 en C++."
type: docs
weight: 10000
url: /es/cpp/aspose.words.saving/htmlsaveoptions/get_documentsplitheadinglevel/
---
## HtmlSaveOptions::get_DocumentSplitHeadingLevel method


Especifica el nivel máximo de encabezados en el que dividir el documento. El valor predeterminado es **%2**.

```cpp
int32_t Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitHeadingLevel() const
```

## Observaciones


Cuando [DocumentSplitCriteria](../get_documentsplitcriteria/) incluye [HeadingParagraph](../../documentsplitcriteria/) y esta propiedad se establece en un valor de 1 a 9, el documento se dividirá en los párrafos formateados con los estilos **Heading 1**, **Heading 2**, **Heading 3**, etc., hasta el nivel de encabezado especificado.

Por defecto, solo los párrafos **Heading 1** y **Heading 2** hacen que el documento se divida. Establecer esta propiedad en cero hará que el documento no se divida en absoluto en los párrafos de encabezado.

## Ejemplos



Muestra cómo dividir un documento HTML de salida por encabezados en varias partes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Cada párrafo que formateamos usando un estilo "Heading" puede servir como encabezado.
// Cada encabezado también puede tener un nivel de encabezado, determinado por el número de su estilo de encabezado.
// Los encabezados a continuación son de los niveles 1-3.
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Heading #1");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 2"));
builder->Writeln(u"Heading #2");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 3"));
builder->Writeln(u"Heading #3");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Heading #4");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 2"));
builder->Writeln(u"Heading #5");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 3"));
builder->Writeln(u"Heading #6");

// Crea un objeto HtmlSaveOptions y establece el criterio de división en "HeadingParagraph".
// Estos criterios dividirán el documento en los párrafos con estilos "Heading" en varios documentos más pequeños,
// y guardarán cada documento en un archivo HTML separado en el sistema de archivos local.
// También estableceremos el nivel máximo de encabezado, lo que divide el documento en 2.
// Al guardar el documento, se dividirá en los encabezados de los niveles 1 y 2, pero no en los del 3 al 9.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_DocumentSplitCriteria(Aspose::Words::Saving::DocumentSplitCriteria::HeadingParagraph);
options->set_DocumentSplitHeadingLevel(2);

// Nuestro documento tiene cuatro encabezados de niveles 1 - 2. Uno de esos encabezados no será
// un punto de división ya que está al comienzo del documento.
// La operación de guardado dividirá nuestro documento en tres lugares, en cuatro documentos más pequeños.
doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels.html", options);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels.html");

ASSERT_EQ(u"Heading #1", doc->GetText().Trim());

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels-01.html");

ASSERT_EQ(System::String(u"Heading #2\r") + u"Heading #3", doc->GetText().Trim());

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels-02.html");

ASSERT_EQ(u"Heading #4", doc->GetText().Trim());

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels-03.html");

ASSERT_EQ(System::String(u"Heading #5\r") + u"Heading #6", doc->GetText().Trim());
```

## Ver también

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
