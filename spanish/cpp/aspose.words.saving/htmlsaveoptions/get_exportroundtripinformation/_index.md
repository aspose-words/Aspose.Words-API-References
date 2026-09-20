---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportRoundtripInformation method"
linktitle: "get_ExportRoundtripInformation"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportRoundtripInformation method. Especifica si se debe escribir la información de ida y vuelta al guardar en HTML, MHTML o EPUB. El valor predeterminado es true para HTML y false para MHTML y EPUB en C++."
type: docs
weight: 26000
url: /es/cpp/aspose.words.saving/htmlsaveoptions/get_exportroundtripinformation/
---
## HtmlSaveOptions::get_ExportRoundtripInformation method


Especifica si se escribe la información de ida y vuelta al guardar en HTML, MHTML o EPUB. El valor predeterminado es **true** para HTML y **false** para MHTML y EPUB.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportRoundtripInformation() const
```

## Observaciones


[Saving](../../) of the roundtrip information allows to restore document properties such as tab stops, comments, headers and footers during the HTML documents loading back into a [Document](../../../aspose.words/document/) object.

Cuando **true**, la información de ida y vuelta se exporta como propiedades CSS -aw-* de los elementos HTML correspondientes.

Cuando **false**, no genera información de ida y vuelta en los archivos producidos.

## Ejemplos



Muestra cómo preservar elementos ocultos al convertir a .html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Al convertir un documento a .html, algunos elementos como marcadores ocultos, posiciones originales de formas,
// o notas al pie serán eliminados o convertidos a texto plano y, efectivamente, se perderán.
// Guardar con un objeto HtmlSaveOptions con ExportRoundtripInformation establecido en true preservará estos elementos.

// Cuando guardamos el documento en HTML, podemos pasar un objeto SaveOptions para determinar
// cómo la operación de guardado exportará los elementos del documento que HTML no soporta o utiliza,
// como marcadores ocultos y posiciones originales de las formas.
// Si establecemos la bandera "ExportRoundtripInformation" a "true", la operación de guardado preservará estos elementos.
// Si establecemos la bandera "ExportRoundTripInformation" a "false", la operación de guardado descartará estos elementos.
// Querremos preservar dichos elementos si pretendemos cargar el HTML guardado usando Aspose.Words,
// ya que podrían ser útiles nuevamente.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportRoundtripInformation(exportRoundtripInformation);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.RoundTripInformation.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.RoundTripInformation.html");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.RoundTripInformation.html");

if (exportRoundtripInformation)
{
    ASSERT_TRUE(outDocContents.Contains(u"<div style=\"-aw-headerfooter-type:header-primary; clear:both\">"));
    ASSERT_TRUE(outDocContents.Contains(u"<span style=\"-aw-import:ignore\">&#xa0;</span>"));

    ASSERT_TRUE(outDocContents.Contains(System::String(u"td colspan=\"2\" style=\"width:210.6pt; border-style:solid; border-width:0.75pt 6pt 0.75pt 0.75pt; ") + u"padding-right:2.4pt; padding-left:5.03pt; vertical-align:top; -aw-border-bottom:0.5pt single #000000; " + u"-aw-border-left:0.5pt single #000000; -aw-border-right:6pt single #000000; -aw-border-top:0.5pt single #000000\">"));

    ASSERT_TRUE(outDocContents.Contains(u"<li style=\"margin-left:30.2pt; padding-left:5.8pt; -aw-font-family:'Courier New'; -aw-font-weight:normal; -aw-number-format:'o'\">"));

    ASSERT_TRUE(outDocContents.Contains(System::String(u"<img src=\"HtmlSaveOptions.RoundTripInformation.003.jpeg\" width=\"350\" height=\"180\" alt=\"\" ") + u"style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />"));

    ASSERT_TRUE(outDocContents.Contains(System::String(u"<span>Page number </span>") + u"<span style=\"-aw-field-start:true\"></span>" + u"<span style=\"-aw-field-code:' PAGE   \\\\* MERGEFORMAT '\"></span>" + u"<span style=\"-aw-field-separator:true\"></span>" + u"<span>1</span>" + u"<span style=\"-aw-field-end:true\"></span>"));

    ASSERT_EQ(1, doc->get_Range()->get_Fields()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fields::Field>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fields::Field> f)>>([](System::SharedPtr<Aspose::Words::Fields::Field> f) -> bool
    {
        return f->get_Type() == Aspose::Words::Fields::FieldType::FieldPage;
    }))));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(u"<div style=\"clear:both\">"));
    ASSERT_TRUE(outDocContents.Contains(u"<span>&#xa0;</span>"));

    ASSERT_TRUE(outDocContents.Contains(System::String(u"<td colspan=\"2\" style=\"width:210.6pt; border-style:solid; border-width:0.75pt 6pt 0.75pt 0.75pt; ") + u"padding-right:2.4pt; padding-left:5.03pt; vertical-align:top\">"));

    ASSERT_TRUE(outDocContents.Contains(u"<li style=\"margin-left:30.2pt; padding-left:5.8pt\">"));

    ASSERT_TRUE(outDocContents.Contains(u"<img src=\"HtmlSaveOptions.RoundTripInformation.003.jpeg\" width=\"350\" height=\"180\" alt=\"\" />"));

    ASSERT_TRUE(outDocContents.Contains(u"<span>Page number 1</span>"));

    ASSERT_EQ(0, doc->get_Range()->get_Fields()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fields::Field>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fields::Field> f)>>([](System::SharedPtr<Aspose::Words::Fields::Field> f) -> bool
    {
        return f->get_Type() == Aspose::Words::Fields::FieldType::FieldPage;
    }))));
}
```

## Ver también

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
