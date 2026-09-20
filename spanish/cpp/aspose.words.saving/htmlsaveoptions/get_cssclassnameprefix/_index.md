---
title: "Método Aspose::Words::Saving::HtmlSaveOptions::get_CssClassNamePrefix"
linktitle: "get_CssClassNamePrefix"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::HtmlSaveOptions::get_CssClassNamePrefix. Especifica un prefijo que se agrega a todos los nombres de clases CSS. El valor predeterminado es una cadena vacía y los nombres de clases CSS generados no tienen un prefijo común en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.saving/htmlsaveoptions/get_cssclassnameprefix/
---
## HtmlSaveOptions::get_CssClassNamePrefix method


Especifica un prefijo que se agrega a todos los nombres de clase CSS. El valor predeterminado es una cadena vacía y los nombres de clase CSS generados no tienen un prefijo común.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_CssClassNamePrefix() const
```

## Observaciones


Si este valor no está vacío, todas las clases CSS generadas por Aspose.Words comenzarán con el prefijo especificado. Esto puede ser útil, por ejemplo, si añades CSS personalizado a los documentos generados y deseas evitar conflictos de nombres de clases.

Si el valor no es **null** o está vacío, debe ser un identificador CSS válido.

## Ejemplos



Muestra cómo guardar un documento en HTML y agregar un prefijo a todos sus nombres de clases CSS.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_CssStyleSheetType(Aspose::Words::Saving::CssStyleSheetType::External);
saveOptions->set_CssClassNamePrefix(u"myprefix-");

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.CssClassNamePrefix.html", saveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.CssClassNamePrefix.html");

ASSERT_TRUE(outDocContents.Contains(u"<p class=\"myprefix-Header\">"));
ASSERT_TRUE(outDocContents.Contains(u"<p class=\"myprefix-Footer\">"));

outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.CssClassNamePrefix.css");

ASSERT_TRUE(outDocContents.Contains(u".myprefix-Footer { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt; -aw-style-name:footer }"));
ASSERT_TRUE(outDocContents.Contains(u".myprefix-Header { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt; -aw-style-name:header }"));
```

## Ver también

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
