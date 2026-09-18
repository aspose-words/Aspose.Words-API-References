---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_TableWidthOutputMode Methode"
linktitle: "get_TableWidthOutputMode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_TableWidthOutputMode Methode. Steuert, wie Tabellen-, Zeilen- und Zellenbreiten nach HTML, MHTML oder EPUB exportiert werden. Standardwert ist All in C++."
type: docs
weight: 47000
url: /de/cpp/aspose.words.saving/htmlsaveoptions/get_tablewidthoutputmode/
---
## HtmlSaveOptions::get_TableWidthOutputMode method


Steuert, wie Tabellen-, Zeilen- und Zellenbreiten nach HTML, MHTML oder EPUB exportiert werden. Standardwert ist [All](../../htmlelementsizeoutputmode/).

```cpp
Aspose::Words::Saving::HtmlElementSizeOutputMode Aspose::Words::Saving::HtmlSaveOptions::get_TableWidthOutputMode() const
```

## Hinweise


Im HTML-Format können Tabellen-, Zeilen- und Zellen-Elemente (**%<table>**, **%<tr>**, **%<th>**, **%<td>**) ihre Breite entweder relativ (Prozent) oder in absoluten Einheiten angegeben bekommen. In einem Dokument in Aspose.Words können Tabellen, Zeilen und Zellen ihre Breite ebenfalls entweder relativ oder absolut angegeben werden.

Wenn Sie ein Dokument mit Aspose.Words nach HTML konvertieren, möchten Sie möglicherweise steuern, wie Tabellen-, Zeilen- und Zellenbreiten exportiert werden, um zu beeinflussen, wie das resultierende Dokument im visuellen Agenten (z. B. einem Browser oder Viewer) angezeigt wird.

Verwenden Sie diese Eigenschaft als Filter, um festzulegen, welche Tabellenbreitenwerte in das Zieldokument exportiert werden. Wenn Sie beispielsweise ein Dokument nach EPUB konvertieren und beabsichtigen, das Dokument auf einem mobilen Lesegerät anzuzeigen, möchten Sie wahrscheinlich das Exportieren absoluter Breitenwerte vermeiden. Dazu müssen Sie den Ausgabemodus [RelativeOnly](../../htmlelementsizeoutputmode/) oder [None](../../htmlelementsizeoutputmode/) festlegen, damit der Viewer auf dem mobilen Gerät die Tabelle bestmöglich an die Bildschirmbreite anpassen kann.

## Beispiele



Zeigt, wie negative Einzüge in der ausgegebenen .html beibehalten werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie eine Tabelle mit einem negativen Einzug ein, der sie nach links über die linke Seitenbegrenzung hinaus verschiebt.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, Cell 1");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2");
builder->EndTable();
table->set_LeftIndent(-36);
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(144));

builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);

// Fügen Sie eine Tabelle mit einem positiven Einzug ein, der die Tabelle nach rechts verschiebt.
table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, Cell 1");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2");
builder->EndTable();
table->set_LeftIndent(36);
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(144));

// Wenn wir ein Dokument als HTML speichern, bewahrt Aspose.Words nur negative Einzüge.
// wie die, die wir auf die erste Tabelle angewendet haben, wenn wir das Flag "AllowNegativeIndent" setzen
// in einem SaveOptions-Objekt, das wir auf "true" übergeben werden
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_AllowNegativeIndent(allowNegativeIndent);
options->set_TableWidthOutputMode(Aspose::Words::Saving::HtmlElementSizeOutputMode::RelativeOnly);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.NegativeIndent.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.NegativeIndent.html");

if (allowNegativeIndent)
{
    ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:-41.65pt; border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
    ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
    ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
}
```

## Siehe auch

* Enum [HtmlElementSizeOutputMode](../../htmlelementsizeoutputmode/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
