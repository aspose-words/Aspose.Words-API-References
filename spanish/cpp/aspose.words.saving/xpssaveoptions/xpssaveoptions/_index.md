---
title: "Constructor Aspose::Words::Saving::XpsSaveOptions::XpsSaveOptions"
linktitle: "XpsSaveOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Constructor Aspose::Words::Saving::XpsSaveOptions::XpsSaveOptions. Inicializa una nueva instancia de esta clase que puede usarse para guardar un documento en formato Xps en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.saving/xpssaveoptions/xpssaveoptions/
---
## XpsSaveOptions::XpsSaveOptions() constructor


Inicializa una nueva instancia de esta clase que puede usarse para guardar un documento en el formato [Xps](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::Saving::XpsSaveOptions::XpsSaveOptions()
```


## Ejemplos



Muestra cómo limitar el nivel de los encabezados que aparecerán en el esquema de un documento XPS guardado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserte encabezados que puedan servir como entradas del índice (TOC) de los niveles 1, 2 y luego 3.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);

ASSERT_TRUE(builder->get_ParagraphFormat()->get_IsHeading());

builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);

builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading3);

builder->Writeln(u"Heading 1.2.1");
builder->Writeln(u"Heading 1.2.2");

// Cree un objeto "XpsSaveOptions" que podamos pasar al método "Save" del documento
// para modificar cómo ese método convierte el documento a .XPS.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::Xps, saveOptions->get_SaveFormat());

// El documento XPS de salida contendrá un esquema, una tabla de contenidos que enumera los encabezados en el cuerpo del documento.
// Al hacer clic en una entrada de este esquema nos llevará a la ubicación de su encabezado correspondiente.
// Establezca la propiedad "HeadingsOutlineLevels" en "2" para excluir todos los encabezados cuyo nivel sea superior a 2 del esquema.
// Los dos últimos encabezados que insertamos arriba no aparecerán.
saveOptions->get_OutlineOptions()->set_HeadingsOutlineLevels(2);

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

## Ver también

* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## XpsSaveOptions::XpsSaveOptions(Aspose::Words::SaveFormat) constructor


Inicializa una nueva instancia de esta clase que puede usarse para guardar un documento en el formato [Xps](../../../aspose.words/saveformat/) o [OpenXps](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::Saving::XpsSaveOptions::XpsSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


## Ejemplos



Muestra cómo guardar un documento en formato XPS en forma de pliegue de libro.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

// Cree un objeto "XpsSaveOptions" que podamos pasar al método "Save" del documento
// para modificar cómo ese método convierte el documento a .XPS.
auto xpsOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>(Aspose::Words::SaveFormat::Xps);

// Establezca la propiedad "UseBookFoldPrintingSettings" a "true" para organizar el contenido
// en el XPS de salida de manera que nos ayude a usarlo para crear un folleto.
// Establezca la propiedad "UseBookFoldPrintingSettings" a "false" para renderizar el XPS normalmente.
xpsOptions->set_UseBookFoldPrintingSettings(renderTextAsBookFold);

// Si estamos renderizando el documento como un folleto, debemos establecer la "MultiplePages"
// propiedades de los objetos de configuración de página de todas las secciones a "MultiplePagesType.BookFoldPrinting".
if (renderTextAsBookFold)
{
    for (auto&& s : System::IterateOver<Aspose::Words::Section>(doc->get_Sections()))
    {
        s->get_PageSetup()->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::BookFoldPrinting);
    }
}

// Una vez que imprimamos este documento, podemos convertirlo en un folleto apilando las páginas
// para salir de la impresora y plegarse por la mitad.
doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.BookFold.xps", xpsOptions);
```

## Ver también

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
