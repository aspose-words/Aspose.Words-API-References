---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitHeadingLevel Methode"
linktitle: "get_DocumentSplitHeadingLevel"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitHeadingLevel Methode. Gibt die maximale Ebene von Überschriften an, bei der das Dokument aufgeteilt wird. Der Standardwert ist %2 in C++."
type: docs
weight: 10000
url: /de/cpp/aspose.words.saving/htmlsaveoptions/get_documentsplitheadinglevel/
---
## HtmlSaveOptions::get_DocumentSplitHeadingLevel method


Gibt die maximale Ebene von Überschriften an, bei der das Dokument aufgeteilt werden soll. Der Standardwert ist **%2**.

```cpp
int32_t Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitHeadingLevel() const
```

## Hinweise


Wenn [DocumentSplitCriteria](../get_documentsplitcriteria/) [HeadingParagraph](../../documentsplitcriteria/) enthält und diese Eigenschaft auf einen Wert von 1 bis 9 gesetzt ist, wird das Dokument an Absätzen aufgeteilt, die mit den Stilen **Heading 1**, **Heading 2**, **Heading 3** usw. bis zur angegebenen Überschriftenebene formatiert sind.

Standardmäßig führen nur **Heading 1**- und **Heading 2**-Absätze dazu, dass das Dokument aufgeteilt wird. Wenn diese Eigenschaft auf Null gesetzt wird, wird das Dokument überhaupt nicht an Überschriftsabsätzen aufgeteilt.

## Beispiele



Zeigt, wie ein ausgegebenes HTML‑Dokument anhand von Überschriften in mehrere Teile aufgeteilt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Jeder Absatz, den wir mit einem "Heading"‑Stil formatieren, kann als Überschrift dienen.
// Jede Überschrift kann zudem eine Ebene haben, die durch die Nummer ihres Überschriftsstils bestimmt wird.
// Die nachstehenden Überschriften haben die Ebenen 1‑3.
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Heading #1");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 2"));
builder->Writeln(u"Heading #2");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 3"));
builder->Writeln(u"Heading #3");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Heading #4");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 2"));
builder->Writeln(u"Heading #5");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 3"));
builder->Writeln(u"Heading #6");

// Erstellen Sie ein HtmlSaveOptions‑Objekt und setzen Sie das Trennkriterium auf "HeadingParagraph".
// Dieses Kriterium teilt das Dokument an Absätzen mit "Heading"‑Stilen in mehrere kleinere Dokumente,
// und speichert jedes Dokument in einer separaten HTML‑Datei im lokalen Dateisystem.
// Wir setzen außerdem die maximale Überschriftsebene, wodurch das Dokument bis Ebene 2 aufgeteilt wird.
// Beim Speichern des Dokuments wird es an Überschriften der Ebenen 1 und 2 aufgeteilt, jedoch nicht an den Ebenen 3 bis 9.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_DocumentSplitCriteria(Aspose::Words::Saving::DocumentSplitCriteria::HeadingParagraph);
options->set_DocumentSplitHeadingLevel(2);

// Unser Dokument enthält vier Überschriften der Ebenen 1 – 2. Eine dieser Überschriften wird nicht
// ein Trennpunkt sein, da sie am Anfang des Dokuments steht.
// Der Speichervorgang wird unser Dokument an drei Stellen aufteilen, in vier kleinere Dokumente.
doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels.html", options);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels.html");

ASSERT_EQ(u"Heading #1", doc->GetText().Trim());

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels-01.html");

ASSERT_EQ(System::String(u"Heading #2\r") + u"Heading #3", doc->GetText().Trim());

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels-02.html");

ASSERT_EQ(u"Heading #4", doc->GetText().Trim());

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels-03.html");

ASSERT_EQ(System::String(u"Heading #5\r") + u"Heading #6", doc->GetText().Trim());
```

## Siehe auch

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
