---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold método"
linktitle: "get_FontResourcesSubsettingSizeThreshold"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold método. Controla qué recursos de fuentes necesitan submuestreo al guardar en HTML, MHTML o EPUB. El valor predeterminado es %0 en C++."
type: docs
weight: 31000
url: /es/cpp/aspose.words.saving/htmlsaveoptions/get_fontresourcessubsettingsizethreshold/
---
## HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold method


Controla qué recursos de fuente requieren subconjunto al guardar en HTML, MHTML o EPUB. El valor predeterminado es **%0**.

```cpp
int32_t Aspose::Words::Saving::HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold() const
```

## Observaciones


[ExportFontResources](../get_exportfontresources/) allows exporting fonts as subsidiary files or as parts of the output package. If the document uses many fonts, especially with large number of glyphs, then output size can grow significantly. [Font](../../../aspose.words/font/) subsetting reduces the size of the exported font resource by filtering out glyphs that are not used by the current document.

[Font](../../../aspose.words/font/) subsetting works as follows:

* By default, all exported fonts are subsetted.
* Setting [FontResourcesSubsettingSizeThreshold](./) to a positive value instructs Aspose.Words to subset fonts which file size is larger than the specified value.
* Setting the property to **MaxValue** suppresses font subsetting.



**Important!** When exporting font resources, font licensing issues should be considered. Authors who want to use specific fonts via a downloadable font mechanism must always carefully verify that their intended use is within the scope of the font license. Many commercial fonts presently do not allow web downloading of their fonts in any form. [License](../../../aspose.words/license/) agreements that cover some fonts specifically note that usage via **%@font-face** rules in CSS style sheets is not allowed. [Font](../../../aspose.words/font/) subsetting can also violate license terms.

## Ejemplos



Muestra cómo trabajar con el submuestreo de fuentes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Times New Roman");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Courier New");
builder->Writeln(u"Hello world!");

// Cuando guardamos el documento en HTML, podemos pasar un objeto SaveOptions para configurar el submuestreo de fuentes.
// Supongamos que establecemos la bandera "ExportFontResources" a "true" y también nombramos una carpeta en la propiedad "FontsFolder".
// En ese caso, la operación de guardado creará esa carpeta y colocará un archivo .ttf dentro.
// esa carpeta para cada fuente que use nuestro documento.
// Cada archivo .ttf contendrá el conjunto completo de glifos de esa fuente,
// lo que puede resultar potencialmente en un archivo muy grande que acompaña al documento.
// Cuando aplicamos submuestreo a una fuente, sus datos brutos exportados solo contendrán los glifos que el documento está
// usando en lugar del conjunto completo de glifos. Si el texto de nuestro documento solo usa una pequeña fracción de la fuente
// conjunto de glifos, entonces el submuestreo reducirá significativamente el tamaño de los documentos de salida.
// Podemos usar la propiedad "FontResourcesSubsettingSizeThreshold" para definir el tamaño de un archivo .ttf, en bytes.
// Si una fuente exportada crea un archivo de mayor tamaño que eso, entonces la operación de guardado aplicará submuestreo a esa fuente.
// Establecer un umbral de 0 aplica submuestreo a todas las fuentes,
// y configurarlo a "int.MaxValue" desactiva efectivamente el subsetting.
System::String fontsFolder = get_ArtifactsDir() + u"HtmlSaveOptions.FontSubsetting.Fonts";

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportFontResources(true);
options->set_FontsFolder(fontsFolder);
options->set_FontResourcesSubsettingSizeThreshold(fontResourcesSubsettingSizeThreshold);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.FontSubsetting.html", options);

System::ArrayPtr<System::String> fontFileNames = System::IO::Directory::GetFiles(fontsFolder)->LINQ_Where(static_cast<System::Func<System::String, bool>>(static_cast<std::function<bool(System::String s)>>([](System::String s) -> bool
{
    return s.EndsWith(u".ttf");
})))->LINQ_ToArray();

ASSERT_EQ(3, fontFileNames->get_Length());

for (System::String filename : fontFileNames)
{
    // Por defecto, los archivos .ttf de cada una de nuestras tres fuentes superarán los 700 MB.
    // El subsetting los reducirá a menos de 30 MB.
    auto fontFileInfo = System::MakeObject<System::IO::FileInfo>(filename);

    ASSERT_TRUE(fontFileInfo->get_Length() > 700000 || fontFileInfo->get_Length() < 30000);
    ASSERT_TRUE(System::Math::Max(fontResourcesSubsettingSizeThreshold, 30000) > System::MakeObject<System::IO::FileInfo>(filename)->get_Length());
}
```

## Ver también

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
