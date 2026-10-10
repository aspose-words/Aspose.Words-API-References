---
title: "Aspose::Words::Layout::LayoutOptions Klasse"
linktitle: "LayoutOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Layout::LayoutOptions Klasse. Enthält die Optionen, die die Steuerung des Dokumentlayout‑Prozesses ermöglichen. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words.layout/layoutoptions/
---
## LayoutOptions class


Enthält die Optionen, die die Steuerung des Dokumentlayout‑Prozesses ermöglichen. Weitere Informationen finden Sie im Dokumentationsartikel [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/).

```cpp
class LayoutOptions : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_Callback](./get_callback/)() const | Liest die Implementierung von [IPageLayoutCallback](../ipagelayoutcallback/), die vom Seitenlayout‑Modell verwendet wird. |
| [get_CommentDisplayMode](./get_commentdisplaymode/)() const | Liest oder schreibt die Art, wie Kommentare dargestellt werden. Der Standardwert ist [ShowInBalloons](../commentdisplaymode/). |
| [get_ContinuousSectionPageNumberingRestart](./get_continuoussectionpagenumberingrestart/)() const | Liest oder schreibt den Verhaltensmodus zur Berechnung von Seitenzahlen, wenn ein fortlaufender Abschnitt die Seitennummerierung neu startet. |
| [get_IgnorePrinterMetrics](./get_ignoreprintermetrics/)() const | Liest oder schreibt die Angabe, ob die Kompatibilitätsoption \"Use printer metrics to lay out document\" ignoriert wird. Der Standardwert ist **true**. |
| [get_KeepOriginalFontMetrics](./get_keeporiginalfontmetrics/)() const | Liest oder schreibt die Angabe, ob nach einer Schriftart‑Ersetzung die ursprünglichen Schriftmetriken verwendet werden sollen. Der Standardwert ist **true**. |
| [get_RevisionOptions](./get_revisionoptions/)() const | Liest die Revisionsoptionen. |
| [get_ShowHiddenText](./get_showhiddentext/)() const | Liest oder schreibt die Angabe, ob versteckter Text im Dokument dargestellt wird. Der Standardwert ist **false**. |
| [get_ShowParagraphMarks](./get_showparagraphmarks/)() const | Liest oder schreibt die Angabe, ob Absatzmarken dargestellt werden. Der Standardwert ist **false**. |
| [get_TextShaperFactory](./get_textshaperfactory/)() const | Liest die Implementierung von [ITextShaperFactory](../), die für erweiterte Typografie‑Renderfunktionen verwendet wird. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LayoutOptions](./layoutoptions/)() |  |
| [set_Callback](./set_callback/)(const System::SharedPtr\<Aspose::Words::Layout::IPageLayoutCallback\>\&) | Setzt die Implementierung von [IPageLayoutCallback](../ipagelayoutcallback/), die vom Seitenlayout‑Modell verwendet wird. |
| [set_CommentDisplayMode](./set_commentdisplaymode/)(Aspose::Words::Layout::CommentDisplayMode) | Setter für [Aspose::Words::Layout::LayoutOptions::get_CommentDisplayMode](./get_commentdisplaymode/). |
| [set_ContinuousSectionPageNumberingRestart](./set_continuoussectionpagenumberingrestart/)(Aspose::Words::Layout::ContinuousSectionRestart) | Setter für [Aspose::Words::Layout::LayoutOptions::get_ContinuousSectionPageNumberingRestart](./get_continuoussectionpagenumberingrestart/). |
| [set_IgnorePrinterMetrics](./set_ignoreprintermetrics/)(bool) | Setter für [Aspose::Words::Layout::LayoutOptions::get_IgnorePrinterMetrics](./get_ignoreprintermetrics/). |
| [set_KeepOriginalFontMetrics](./set_keeporiginalfontmetrics/)(bool) | Setter für [Aspose::Words::Layout::LayoutOptions::get_KeepOriginalFontMetrics](./get_keeporiginalfontmetrics/). |
| [set_ShowHiddenText](./set_showhiddentext/)(bool) | Setter für [Aspose::Words::Layout::LayoutOptions::get_ShowHiddenText](./get_showhiddentext/). |
| [set_ShowParagraphMarks](./set_showparagraphmarks/)(bool) | Setter für [Aspose::Words::Layout::LayoutOptions::get_ShowParagraphMarks](./get_showparagraphmarks/). |
| [set_TextShaperFactory](./set_textshaperfactory/)(const System::SharedPtr\<Aspose::Words::Shaping::ITextShaperFactory\>\&) | Legt die [ITextShaperFactory](../)-Implementierung fest, die für erweiterte Typografie‑Renderfunktionen verwendet wird. |
| static [Type](./type/)() |  |
## Hinweise


Sie erstellen keine Instanzen dieser Klasse direkt. Verwenden Sie die [LayoutOptions](../../aspose.words/document/get_layoutoptions/)-Eigenschaft, um auf die Layout‑Optionen dieses Dokuments zuzugreifen.

Beachten Sie, dass nach dem Ändern einer der in dieser Klasse vorhandenen Optionen die [UpdatePageLayout](../../aspose.words/document/updatepagelayout/)-Methode aufgerufen werden muss, damit die geänderten Optionen auf das Layout angewendet werden.

## Beispiele



Zeigt, wie man Text in einem gerenderten Ausgabedokument ausblendet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie versteckten Text ein und geben Sie dann an, ob wir ihn aus einem gerenderten Dokument weglassen möchten.
builder->Writeln(u"This text is not hidden.");
builder->get_Font()->set_Hidden(true);
builder->Writeln(u"This text is hidden.");

doc->get_LayoutOptions()->set_ShowHiddenText(showHiddenText);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsHiddenText.pdf");
```


Zeigt, wie man Absatzmarken in einem gerenderten Ausgabedokument anzeigt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie einige Absätze hinzu und aktivieren Sie dann Absatzmarken, um das Ende der Absätze anzuzeigen
// mit einem Pilcrow‑Symbol (¶), wenn wir das Dokument rendern.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

doc->get_LayoutOptions()->set_ShowParagraphMarks(showParagraphMarks);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsParagraphMarks.pdf");
```


Zeigt, wie man das Aussehen von Revisionen in einem gerenderten Ausgabedokument ändert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie eine Revision ein und ändern Sie dann die Farbe aller Revisionen zu Grün.
builder->Writeln(u"This is not a revision.");
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
builder->Writeln(u"This is a revision.");
doc->StopTrackRevisions();
builder->Writeln(u"This is not a revision.");

// Entfernen Sie die Leiste, die links von jeder überarbeiteten Zeile erscheint.
doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertedTextColor(Aspose::Words::Layout::RevisionColor::BrightGreen);
doc->get_LayoutOptions()->get_RevisionOptions()->set_ShowRevisionBars(false);
doc->get_LayoutOptions()->get_RevisionOptions()->set_RevisionBarsPosition(Aspose::Words::Drawing::HorizontalAlignment::Right);

doc->Save(get_ArtifactsDir() + u"Revision.LayoutOptionsRevisions.pdf");
```

## Siehe auch

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
