---
title: "Aspose::Words::Saving::HtmlElementSizeOutputMode enum"
linktitle: "HtmlElementSizeOutputMode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlElementSizeOutputMode enum. Gibt an, wie Aspose.Words Elementbreiten und -höhen nach HTML, MHTML und EPUB in C++ exportiert."
type: docs
weight: 58000
url: /de/cpp/aspose.words.saving/htmlelementsizeoutputmode/
---
## HtmlElementSizeOutputMode enum


Gibt an, wie Aspose.Words Elementbreiten und -höhen nach HTML, MHTML und EPUB exportiert.

```cpp
enum class HtmlElementSizeOutputMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Alle | 0 | Alle Elementgrößen, sowohl in absoluten als auch in relativen Einheiten, die im Dokument angegeben sind, werden exportiert. |
| RelativeOnly | 1 | Elementgrößen werden nur exportiert, wenn sie im Dokument in relativen Einheiten angegeben sind. Feste Größen werden in diesem Modus nicht exportiert. Visuelle Agenten berechnen fehlende Größen, um das Dokumentlayout natürlicher zu gestalten. |
| Keine | 2 | Elementgrößen werden nicht exportiert. Visuelle Agenten erstellen das Layout automatisch basierend auf der Beziehung zwischen den Elementen. |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
