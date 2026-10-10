---
title: "Aspose::Words::Layout::RevisionOptions class"
linktitle: "RevisionOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Layout::RevisionOptions class. Ermöglicht die Steuerung, wie Dokumentrevisionen während des Layout‑Vorgangs verarbeitet werden. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words.layout/revisionoptions/
---
## RevisionOptions class


Ermöglicht die Steuerung, wie Dokumentrevisionen während des Layout‑Prozesses behandelt werden. Weitere Informationen finden Sie im Dokumentationsartikel [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/).

```cpp
class RevisionOptions : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_CommentColor](./get_commentcolor/)() const | Ermöglicht die Angabe der Farbe, die für Kommentare verwendet wird. Standardwert ist [Red](../revisioncolor/). |
| [get_DeleteCellColor](./get_deletecellcolor/)() | Ermöglicht die Angabe der Farbe, die für gelöschte Zellen verwendet wird [Deletion](../../aspose.words/revisiontype/). Standardwert ist [Pink](../revisioncolor/). |
| [get_DeletedTextColor](./get_deletedtextcolor/)() | Ermöglicht die Angabe der Farbe, die für gelöschten Inhalt verwendet wird [Deletion](../../aspose.words/revisiontype/). Standardwert ist [ByAuthor](../revisioncolor/). |
| [get_DeletedTextEffect](./get_deletedtexteffect/)() | Ermöglicht die Angabe des Effekts, der auf gelöschten Inhalt angewendet wird [Deletion](../../aspose.words/revisiontype/). Standardwert ist [StrikeThrough](../revisiontexteffect/) |
| [get_InsertCellColor](./get_insertcellcolor/)() | Ermöglicht die Angabe der Farbe, die für eingefügte Zellen verwendet wird [Insertion](../../aspose.words/revisiontype/). Standardwert ist [Blue](../revisioncolor/). |
| [get_InsertedTextColor](./get_insertedtextcolor/)() | Ermöglicht die Angabe der Farbe, die für eingefügten Inhalt verwendet wird [Insertion](../../aspose.words/revisiontype/). Standardwert ist [ByAuthor](../revisioncolor/). |
| [get_InsertedTextEffect](./get_insertedtexteffect/)() | Ermöglicht die Angabe des Effekts, der auf eingefügten Inhalt angewendet wird [Insertion](../../aspose.words/revisiontype/). Standardwert ist [Underline](../revisiontexteffect/). |
| [get_MeasurementUnit](./get_measurementunit/)() const | Ermöglicht die Angabe der Maßeinheiten für Revisionskommentare. Standardwert ist [Centimeters](../../aspose.words/measurementunits/) |
| [get_MovedFromTextColor](./get_movedfromtextcolor/)() | Ermöglicht die Angabe der Farbe, die für Bereiche verwendet wird, aus denen Inhalt verschoben wurde [Moving](../../aspose.words/revisiontype/). Standardwert ist [ByAuthor](../revisioncolor/). |
| [get_MovedFromTextEffect](./get_movedfromtexteffect/)() | Ermöglicht die Angabe des Effekts, der auf Bereiche angewendet wird, aus denen Inhalt verschoben wurde [Moving](../../aspose.words/revisiontype/). Standardwert ist [DoubleStrikeThrough](../revisiontexteffect/) |
| [get_MovedToTextColor](./get_movedtotextcolor/)() | Ermöglicht die Angabe der Farbe, die für Bereiche verwendet wird, in die Inhalt verschoben wurde [Moving](../../aspose.words/revisiontype/). Standardwert ist [ByAuthor](../revisioncolor/). |
| [get_MovedToTextEffect](./get_movedtotexteffect/)() | Ermöglicht die Angabe des Effekts, der auf Bereiche angewendet wird, in die Inhalt verschoben wurde [Moving](../../aspose.words/revisiontype/). Standardwert ist [DoubleUnderline](../revisiontexteffect/) |
| [get_RevisedPropertiesColor](./get_revisedpropertiescolor/)() | Ermöglicht die Angabe der Farbe, die für Inhalte mit Änderungen von Formatierungseigenschaften verwendet wird [FormatChange](../../aspose.words/revisiontype/) Standardwert ist [NoHighlight](../revisioncolor/). |
| [get_RevisedPropertiesEffect](./get_revisedpropertieseffect/)() | Ermöglicht die Angabe des Effekts für Inhaltsbereiche mit Änderungen von Formatierungseigenschaften [FormatChange](../../aspose.words/revisiontype/) Der Standardwert ist [None](../revisiontexteffect/) |
| [get_RevisionBarsColor](./get_revisionbarscolor/)() const | Ermöglicht die Angabe der Farbe, die für Seitenleisten verwendet wird, die Dokumentzeilen mit überarbeiteten Informationen kennzeichnen. Der Standardwert ist [Red](../revisioncolor/). |
| [get_RevisionBarsPosition](./get_revisionbarsposition/)() const | Liest oder legt die Renderposition der Revisionsbalken fest. Der Standardwert ist [Outside](../../aspose.words.drawing/horizontalalignment/). |
| [get_RevisionBarsWidth](./get_revisionbarswidth/)() const | Liest oder legt die Breite der Revisionsbalken in Punkten fest. |
| [get_ShowInBalloons](./get_showinballoons/)() const | Ermöglicht die Angabe, ob die Revisionen in den Ballons dargestellt werden. Der Standardwert ist [None](../showinballoons/). |
| [get_ShowOriginalRevision](./get_showoriginalrevision/)() const | Ermöglicht die Angabe, ob der Originaltext anstelle des überarbeiteten angezeigt werden soll. Der Standardwert ist **false**. |
| [get_ShowRevisionBars](./get_showrevisionbars/)() const | Ermöglicht die Angabe, ob Revisionsbalken in der Nähe von Zeilen mit überarbeitetem Inhalt dargestellt werden sollen. Der Standardwert ist **true**. |
| [get_ShowRevisionMarks](./get_showrevisionmarks/)() const | Ermöglicht die Angabe, ob Revisionstext mit spezieller Formatierungskennzeichnung markiert werden soll. Der Standardwert ist **true**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CommentColor](./set_commentcolor/)(Aspose::Words::Layout::RevisionColor) | Setter für [Aspose::Words::Layout::RevisionOptions::get_CommentColor](./get_commentcolor/). |
| [set_DeleteCellColor](./set_deletecellcolor/)(Aspose::Words::Layout::RevisionColor) | Setter für [Aspose::Words::Layout::RevisionOptions::get_DeleteCellColor](./get_deletecellcolor/). |
| [set_DeletedTextColor](./set_deletedtextcolor/)(Aspose::Words::Layout::RevisionColor) | Setter für [Aspose::Words::Layout::RevisionOptions::get_DeletedTextColor](./get_deletedtextcolor/). |
| [set_DeletedTextEffect](./set_deletedtexteffect/)(Aspose::Words::Layout::RevisionTextEffect) | Setter für [Aspose::Words::Layout::RevisionOptions::get_DeletedTextEffect](./get_deletedtexteffect/). |
| [set_InsertCellColor](./set_insertcellcolor/)(Aspose::Words::Layout::RevisionColor) | Setter für [Aspose::Words::Layout::RevisionOptions::get_InsertCellColor](./get_insertcellcolor/). |
| [set_InsertedTextColor](./set_insertedtextcolor/)(Aspose::Words::Layout::RevisionColor) | Setter für [Aspose::Words::Layout::RevisionOptions::get_InsertedTextColor](./get_insertedtextcolor/). |
| [set_InsertedTextEffect](./set_insertedtexteffect/)(Aspose::Words::Layout::RevisionTextEffect) | Setter für [Aspose::Words::Layout::RevisionOptions::get_InsertedTextEffect](./get_insertedtexteffect/). |
| [set_MeasurementUnit](./set_measurementunit/)(Aspose::Words::MeasurementUnits) | Ermöglicht die Angabe der Maßeinheiten für Revisionskommentare. Standardwert ist [Centimeters](../../aspose.words/measurementunits/) |
| [set_MovedFromTextColor](./set_movedfromtextcolor/)(Aspose::Words::Layout::RevisionColor) | Setter für [Aspose::Words::Layout::RevisionOptions::get_MovedFromTextColor](./get_movedfromtextcolor/). |
| [set_MovedFromTextEffect](./set_movedfromtexteffect/)(Aspose::Words::Layout::RevisionTextEffect) | Setter für [Aspose::Words::Layout::RevisionOptions::get_MovedFromTextEffect](./get_movedfromtexteffect/). |
| [set_MovedToTextColor](./set_movedtotextcolor/)(Aspose::Words::Layout::RevisionColor) | Setter für [Aspose::Words::Layout::RevisionOptions::get_MovedToTextColor](./get_movedtotextcolor/). |
| [set_MovedToTextEffect](./set_movedtotexteffect/)(Aspose::Words::Layout::RevisionTextEffect) | Setter für [Aspose::Words::Layout::RevisionOptions::get_MovedToTextEffect](./get_movedtotexteffect/). |
| [set_RevisedPropertiesColor](./set_revisedpropertiescolor/)(Aspose::Words::Layout::RevisionColor) | Setter für [Aspose::Words::Layout::RevisionOptions::get_RevisedPropertiesColor](./get_revisedpropertiescolor/). |
| [set_RevisedPropertiesEffect](./set_revisedpropertieseffect/)(Aspose::Words::Layout::RevisionTextEffect) | Setter für [Aspose::Words::Layout::RevisionOptions::get_RevisedPropertiesEffect](./get_revisedpropertieseffect/). |
| [set_RevisionBarsColor](./set_revisionbarscolor/)(Aspose::Words::Layout::RevisionColor) | Setter für [Aspose::Words::Layout::RevisionOptions::get_RevisionBarsColor](./get_revisionbarscolor/). |
| [set_RevisionBarsPosition](./set_revisionbarsposition/)(Aspose::Words::Drawing::HorizontalAlignment) | Setter für [Aspose::Words::Layout::RevisionOptions::get_RevisionBarsPosition](./get_revisionbarsposition/). |
| [set_RevisionBarsWidth](./set_revisionbarswidth/)(float) | Setter für [Aspose::Words::Layout::RevisionOptions::get_RevisionBarsWidth](./get_revisionbarswidth/). |
| [set_ShowInBalloons](./set_showinballoons/)(Aspose::Words::Layout::ShowInBalloons) | Setter für [Aspose::Words::Layout::RevisionOptions::get_ShowInBalloons](./get_showinballoons/). |
| [set_ShowOriginalRevision](./set_showoriginalrevision/)(bool) | Setter für [Aspose::Words::Layout::RevisionOptions::get_ShowOriginalRevision](./get_showoriginalrevision/). |
| [set_ShowRevisionBars](./set_showrevisionbars/)(bool) | Setter für [Aspose::Words::Layout::RevisionOptions::get_ShowRevisionBars](./get_showrevisionbars/). |
| [set_ShowRevisionMarks](./set_showrevisionmarks/)(bool) | Setter für [Aspose::Words::Layout::RevisionOptions::get_ShowRevisionMarks](./get_showrevisionmarks/). |
| static [Type](./type/)() |  |

## Beispiele



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
