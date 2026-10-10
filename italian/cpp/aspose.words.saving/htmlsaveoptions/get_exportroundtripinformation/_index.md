---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportRoundtripInformation metodo"
linktitle: "get_ExportRoundtripInformation"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportRoundtripInformation metodo. Specifica se scrivere le informazioni di roundtrip durante il salvataggio in HTML, MHTML o EPUB. Il valore predefinito è true per HTML e false per MHTML e EPUB in C++."
type: docs
weight: 26000
url: /it/cpp/aspose.words.saving/htmlsaveoptions/get_exportroundtripinformation/
---
## HtmlSaveOptions::get_ExportRoundtripInformation method


Specifica se scrivere le informazioni di roundtrip durante il salvataggio in HTML, MHTML o EPUB. Il valore predefinito è **true** per HTML e **false** per MHTML e EPUB.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportRoundtripInformation() const
```

## Note


[Saving](../../) of the roundtrip information allows to restore document properties such as tab stops, comments, headers and footers during the HTML documents loading back into a [Document](../../../aspose.words/document/) object.

Quando **true**, le informazioni di roundtrip vengono esportate come proprietà CSS -aw-* degli elementi HTML corrispondenti.

Quando **false**, non genera alcuna informazione di roundtrip nei file prodotti.

## Esempi



Mostra come preservare gli elementi nascosti durante la conversione in .html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Durante la conversione di un documento in .html, alcuni elementi come segnalibri nascosti, posizioni originali delle forme,
// o le note a piè di pagina verranno rimossi o convertiti in testo semplice e andranno persi.
// Il salvataggio con un oggetto HtmlSaveOptions con ExportRoundtripInformation impostato su true preserva questi elementi.

// Quando salviamo il documento in HTML, possiamo passare un oggetto SaveOptions per determinare
// come l'operazione di salvataggio esporterà gli elementi del documento che HTML non supporta o utilizza,
// come segnalibri nascosti e posizioni originali delle forme.
// Se impostiamo il flag "ExportRoundtripInformation" su "true", l'operazione di salvataggio conserverà questi elementi.
// Se impostiamo il flag "ExportRoundTripInformation" su "false", l'operazione di salvataggio scarterà questi elementi.
// Vogliamo conservare tali elementi se intendiamo caricare l'HTML salvato usando Aspose.Words,
// poiché potrebbero tornare utili.
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

## Vedi anche

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
