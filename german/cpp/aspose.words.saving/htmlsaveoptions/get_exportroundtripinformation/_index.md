---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportRoundtripInformation Methode"
linktitle: "get_ExportRoundtripInformation"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportRoundtripInformation Methode. Gibt an, ob die Round‑Trip‑Informationen beim Speichern nach HTML, MHTML oder EPUB geschrieben werden sollen. Der Standardwert ist true für HTML und false für MHTML und EPUB in C++."
type: docs
weight: 26000
url: /de/cpp/aspose.words.saving/htmlsaveoptions/get_exportroundtripinformation/
---
## HtmlSaveOptions::get_ExportRoundtripInformation method


Gibt an, ob die Roundtrip-Informationen beim Speichern nach HTML, MHTML oder EPUB geschrieben werden sollen. Standardwert ist **true** für HTML und **false** für MHTML und EPUB.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportRoundtripInformation() const
```

## Hinweise


[Saving](../../) of the roundtrip information allows to restore document properties such as tab stops, comments, headers and footers during the HTML documents loading back into a [Document](../../../aspose.words/document/) object.

Wenn **true**, werden die Round‑Trip‑Informationen als -aw-* CSS‑Eigenschaften der entsprechenden HTML‑Elemente exportiert.

Wenn **false**, werden keine Roundtrip-Informationen in die erzeugten Dateien ausgegeben.

## Beispiele



Zeigt, wie versteckte Elemente beim Konvertieren zu .html erhalten bleiben.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Beim Konvertieren eines Dokuments zu .html werden einige Elemente wie versteckte Lesezeichen, ursprüngliche Formpositionen,
// oder Fußnoten entweder entfernt oder in Klartext umgewandelt und damit effektiv verloren gehen.
// Das Speichern mit einem HtmlSaveOptions-Objekt, bei dem ExportRoundtripInformation auf true gesetzt ist, bewahrt diese Elemente.

// Wenn wir das Dokument als HTML speichern, können wir ein SaveOptions-Objekt übergeben, um zu bestimmen
// wie der Speichervorgang Dokumentelemente exportiert, die HTML nicht unterstützt oder verwendet,
// wie versteckte Lesezeichen und ursprüngliche Formpositionen.
// Wenn wir das Flag "ExportRoundtripInformation" auf "true" setzen, wird der Speichervorgang diese Elemente bewahren.
// Wenn wir das Flag "ExportRoundTripInformation" auf "false" setzen, wird der Speichervorgang diese Elemente verwerfen.
// Wir möchten solche Elemente erhalten, wenn wir beabsichtigen, das gespeicherte HTML mit Aspose.Words zu laden,
// da sie erneut nützlich sein könnten.
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

## Siehe auch

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
