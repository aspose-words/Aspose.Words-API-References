---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportXhtmlTransitional método"
linktitle: "get_ExportXhtmlTransitional"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportXhtmlTransitional método. Especifica si se debe escribir la declaración DOCTYPE al guardar en HTML o MHTML. Cuando es true, escribe una declaración DOCTYPE en el documento antes del elemento raíz. El valor predeterminado es false. Al guardar en EPUB o HTML5 (Html5) la declaración DOCTYPE siempre se escribe en C++."
type: docs
weight: 30000
url: /es/cpp/aspose.words.saving/htmlsaveoptions/get_exportxhtmltransitional/
---
## HtmlSaveOptions::get_ExportXhtmlTransitional method


Especifica si se debe escribir la declaración DOCTYPE al guardar en HTML o MHTML. Cuando **true**, escribe una declaración DOCTYPE en el documento antes del elemento raíz. El valor predeterminado es **false**. Al guardar en EPUB o HTML5 ([Html5](../../htmlversion/)) la declaración DOCTYPE siempre se escribe.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportXhtmlTransitional() const
```

## Observaciones


Aspose.Words siempre escribe HTML bien formado sin importar esta configuración.

Cuando **true**, el comienzo del documento HTML de salida se verá así:


```cpp
<?xml version="1.0" encoding="utf-8" standalone="no" ?>
             <!DOCTYPE html
                   PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
             "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
             <html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
```


Aspose.Words pretende generar XHTML de acuerdo con la especificación XHTML 1.0 Transitional, pero la salida no siempre validará contra el DTD. Algunas estructuras dentro de un documento de Microsoft Word son difíciles o imposibles de mapear a un documento que valide contra el esquema XHTML. Por ejemplo, XHTML no permite listas anidadas (UL no puede estar anidado dentro de otro elemento UL), pero en los documentos de Microsoft Word las listas multinivel aparecen con frecuencia.

## Ejemplos



Muestra cómo mostrar una cabecera DOCTYPE al convertir documentos al estándar Xhtml 1.0 transitional.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_HtmlVersion(Aspose::Words::Saving::HtmlVersion::Xhtml);
options->set_ExportXhtmlTransitional(showDoctypeDeclaration);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportXhtmlTransitional.html", options);

// Nuestro documento solo contendrá una cabecera de declaración DOCTYPE si hemos configurado la bandera "ExportXhtmlTransitional" a "true".
System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportXhtmlTransitional.html");
System::String newLine = System::Environment::get_NewLine();

if (showDoctypeDeclaration)
{
    ASSERT_TRUE(outDocContents.Contains(System::String::Format(u"<?xml version=\"1.0\" encoding=\"utf-8\" standalone=\"no\"?>{0}", newLine) + System::String::Format(u"<!DOCTYPE html PUBLIC \"-//W3C//DTD XHTML 1.0 Transitional//EN\" \"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd\">{0}", newLine) + u"<html xmlns=\"http://www.w3.org/1999/xhtml\">"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(u"<html>"));
}
```

## Ver también

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
