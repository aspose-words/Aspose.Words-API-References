---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold metodo"
linktitle: "get_FontResourcesSubsettingSizeThreshold"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold metodo. Controlla quali risorse di carattere necessitano di subsetting durante il salvataggio in HTML, MHTML o EPUB. Il valore predefinito è %0 in C++."
type: docs
weight: 31000
url: /it/cpp/aspose.words.saving/htmlsaveoptions/get_fontresourcessubsettingsizethreshold/
---
## HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold method


Controlla quali risorse di carattere richiedono il subset durante il salvataggio in HTML, MHTML o EPUB. Il valore predefinito è **%0**.

```cpp
int32_t Aspose::Words::Saving::HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold() const
```

## Note


[ExportFontResources](../get_exportfontresources/) allows exporting fonts as subsidiary files or as parts of the output package. If the document uses many fonts, especially with large number of glyphs, then output size can grow significantly. [Font](../../../aspose.words/font/) subsetting reduces the size of the exported font resource by filtering out glyphs that are not used by the current document.

[Font](../../../aspose.words/font/) subsetting works as follows:

* By default, all exported fonts are subsetted.
* Setting [FontResourcesSubsettingSizeThreshold](./) to a positive value instructs Aspose.Words to subset fonts which file size is larger than the specified value.
* Setting the property to **MaxValue** suppresses font subsetting.



**Important!** When exporting font resources, font licensing issues should be considered. Authors who want to use specific fonts via a downloadable font mechanism must always carefully verify that their intended use is within the scope of the font license. Many commercial fonts presently do not allow web downloading of their fonts in any form. [License](../../../aspose.words/license/) agreements that cover some fonts specifically note that usage via **%@font-face** rules in CSS style sheets is not allowed. [Font](../../../aspose.words/font/) subsetting can also violate license terms.

## Esempi



Mostra come lavorare con il subsetting dei caratteri.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Times New Roman");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Courier New");
builder->Writeln(u"Hello world!");

// Quando salviamo il documento in HTML, possiamo passare un oggetto SaveOptions per configurare il subsetting dei caratteri.
// Supponiamo di impostare il flag "ExportFontResources" su "true" e di specificare anche una cartella nella proprietà "FontsFolder".
// In tal caso, l'operazione di salvataggio creerà quella cartella e vi inserirà un file .ttf all'interno
// quella cartella per ogni carattere utilizzato dal nostro documento.
// Ogni file .ttf conterrà l'intero set di glifi di quel carattere,
// il che può potenzialmente generare un file molto grande che accompagna il documento.
// Quando applichiamo il subsetting a un carattere, i suoi dati grezzi esportati conterranno solo i glifi che il documento è
// utilizza invece dell'intero set di glifi. Se il testo nel nostro documento utilizza solo una piccola frazione del set di glifi di un carattere
// allora il subsetting ridurrà significativamente le dimensioni dei nostri documenti di output.
// Possiamo utilizzare la proprietà "FontResourcesSubsettingSizeThreshold" per definire una dimensione di file .ttf, in byte.
// Se un carattere esportato crea un file di dimensioni maggiori di quello, allora l'operazione di salvataggio applicherà il subsetting a quel carattere.
// Impostare una soglia di 0 applica il subsetting a tutti i caratteri,
// e impostandolo su "int.MaxValue" disabilita efficacemente il sottoinsieme.
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
    // Per impostazione predefinita, i file .ttf per ciascuno dei nostri tre font supereranno i 700 MB.
    // Il sottoinsieme li ridurrà tutti a meno di 30 MB.
    auto fontFileInfo = System::MakeObject<System::IO::FileInfo>(filename);

    ASSERT_TRUE(fontFileInfo->get_Length() > 700000 || fontFileInfo->get_Length() < 30000);
    ASSERT_TRUE(System::Math::Max(fontResourcesSubsettingSizeThreshold, 30000) > System::MakeObject<System::IO::FileInfo>(filename)->get_Length());
}
```

## Vedi anche

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
