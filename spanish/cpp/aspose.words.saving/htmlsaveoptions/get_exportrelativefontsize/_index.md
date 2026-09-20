---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportRelativeFontSize método"
linktitle: "get_ExportRelativeFontSize"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportRelativeFontSize método. Especifica si los tamaños de fuente deben emitirse en unidades relativas al guardar en HTML, MHTML o EPUB. El valor predeterminado es false en C++."
type: docs
weight: 25000
url: /es/cpp/aspose.words.saving/htmlsaveoptions/get_exportrelativefontsize/
---
## HtmlSaveOptions::get_ExportRelativeFontSize method


Especifica si los tamaños de fuente deben exportarse en unidades relativas al guardar en HTML, MHTML o EPUB. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportRelativeFontSize() const
```

## Observaciones


En muchos documentos existentes (HTML, IDPF EPUB) los tamaños de fuente se especifican en unidades relativas. Esto permite que las aplicaciones ajusten el tamaño del texto al ver o procesar documentos. Por ejemplo, Microsoft Internet Explorer tiene el submenú "Ver->Tamaño del texto", Adobe Digital Editions tiene dos botones: Aumentar/Disminuir tamaño del texto. Si esperas que esta funcionalidad funcione, entonces establece la propiedad [ExportRelativeFontSize](./) a **true**.

**Aspose**[Words](../../../aspose.words/) document model contains and operates only with absolute font size units. Relative units need additional logic to be recalculated from some initial (standard) size. [Font](../../../aspose.words/font/) size of **Normal** document style is taken as standard. For instance, if **Normal** has 12pt font and some text is 18pt then it will be output as **%1.5em.** to the HTML.

Cuando esta opción está habilitada, los elementos del documento que no sean texto seguirán teniendo tamaños absolutos. Además, algunos atributos relacionados con el texto pueden expresarse de forma absoluta. En particular, el interlineado especificado con la regla "exactamente" podría producir resultados no deseados al escalar el texto. Por lo tanto, los documentos de origen deben estar diseñados y probados adecuadamente al exportar con [ExportRelativeFontSize](./) establecido en **true**.

## Ejemplos



Muestra cómo usar tamaños de fuente relativos al guardar en .html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Default font size, ");
builder->get_Font()->set_Size(24);
builder->Writeln(u"2x default font size,");
builder->get_Font()->set_Size(96);
builder->Write(u"8x default font size");

// Cuando guardamos el documento en HTML, podemos pasar un objeto SaveOptions
// para determinar si usar tamaños de fuente relativos o absolutos.
// Establece la bandera "ExportRelativeFontSize" a "true" para declarar los tamaños de fuente
// usando la unidad de medida "em", que es un factor que multiplica el tamaño de fuente actual.
// Establece la bandera "ExportRelativeFontSize" a "false" para declarar los tamaños de fuente
// usando la unidad de medida "pt", que es el tamaño absoluto de la fuente en puntos.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportRelativeFontSize(exportRelativeFontSize);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.RelativeFontSize.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.RelativeFontSize.html");

if (exportRelativeFontSize)
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<body style=\"font-family:'Times New Roman'\">") + u"<div>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt\">" + u"<span>Default font size, </span>" + u"</p>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:2em\">" + u"<span>2x default font size,</span>" + u"</p>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:8em\">" + u"<span>8x default font size</span>" + u"</p>" + u"</div>" + u"</body>"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<body style=\"font-family:'Times New Roman'; font-size:12pt\">") + u"<div>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt\">" + u"<span>Default font size, </span>" + u"</p>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:24pt\">" + u"<span>2x default font size,</span>" + u"</p>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:96pt\">" + u"<span>8x default font size</span>" + u"</p>" + u"</div>" + u"</body>"));
}
```

## Ver también

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
