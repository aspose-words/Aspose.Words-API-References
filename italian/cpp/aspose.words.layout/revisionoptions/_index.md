---
title: "Aspose::Words::Layout::RevisionOptions classe"
linktitle: "RevisionOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Layout::RevisionOptions classe. Consente di controllare come le revisioni del documento vengono gestite durante il processo di layout. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.layout/revisionoptions/
---
## RevisionOptions class


Consente di controllare come le revisioni del documento vengono gestite durante il processo di layout. Per saperne di più, visita l'articolo di documentazione [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/).

```cpp
class RevisionOptions : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_CommentColor](./get_commentcolor/)() const | Consente di specificare il colore da utilizzare per i commenti. Il valore predefinito è [Red](../revisioncolor/). |
| [get_DeleteCellColor](./get_deletecellcolor/)() | Consente di specificare il colore da utilizzare per le celle eliminate [Deletion](../../aspose.words/revisiontype/). Il valore predefinito è [Pink](../revisioncolor/). |
| [get_DeletedTextColor](./get_deletedtextcolor/)() | Consente di specificare il colore da utilizzare per il contenuto eliminato [Deletion](../../aspose.words/revisiontype/). Il valore predefinito è [ByAuthor](../revisioncolor/). |
| [get_DeletedTextEffect](./get_deletedtexteffect/)() | Consente di specificare l'effetto da applicare al contenuto eliminato [Deletion](../../aspose.words/revisiontype/). Il valore predefinito è [StrikeThrough](../revisiontexteffect/) |
| [get_InsertCellColor](./get_insertcellcolor/)() | Consente di specificare il colore da utilizzare per le celle inserite [Insertion](../../aspose.words/revisiontype/). Il valore predefinito è [Blue](../revisioncolor/). |
| [get_InsertedTextColor](./get_insertedtextcolor/)() | Consente di specificare il colore da utilizzare per il contenuto inserito [Insertion](../../aspose.words/revisiontype/). Il valore predefinito è [ByAuthor](../revisioncolor/). |
| [get_InsertedTextEffect](./get_insertedtexteffect/)() | Consente di specificare l'effetto da applicare al contenuto inserito [Insertion](../../aspose.words/revisiontype/). Il valore predefinito è [Underline](../revisiontexteffect/). |
| [get_MeasurementUnit](./get_measurementunit/)() const | Consente di specificare le unità di misura per i commenti di revisione. Il valore predefinito è [Centimeters](../../aspose.words/measurementunits/) |
| [get_MovedFromTextColor](./get_movedfromtextcolor/)() | Consente di specificare il colore da utilizzare per le aree da cui è stato spostato il contenuto [Moving](../../aspose.words/revisiontype/). Il valore predefinito è [ByAuthor](../revisioncolor/). |
| [get_MovedFromTextEffect](./get_movedfromtexteffect/)() | Consente di specificare l'effetto da applicare alle aree da cui è stato spostato il contenuto [Moving](../../aspose.words/revisiontype/). Il valore predefinito è [DoubleStrikeThrough](../revisiontexteffect/) |
| [get_MovedToTextColor](./get_movedtotextcolor/)() | Consente di specificare il colore da utilizzare per le aree verso cui è stato spostato il contenuto [Moving](../../aspose.words/revisiontype/). Il valore predefinito è [ByAuthor](../revisioncolor/). |
| [get_MovedToTextEffect](./get_movedtotexteffect/)() | Consente di specificare l'effetto da applicare alle aree verso cui è stato spostato il contenuto [Moving](../../aspose.words/revisiontype/). Il valore predefinito è [DoubleUnderline](../revisiontexteffect/) |
| [get_RevisedPropertiesColor](./get_revisedpropertiescolor/)() | Consente di specificare il colore da utilizzare per il contenuto con modifiche delle proprietà di formattazione [FormatChange](../../aspose.words/revisiontype/) Il valore predefinito è [NoHighlight](../revisioncolor/). |
| [get_RevisedPropertiesEffect](./get_revisedpropertieseffect/)() | Consente di specificare l'effetto per le aree di contenuto con modifiche delle proprietà di formattazione [FormatChange](../../aspose.words/revisiontype/) Il valore predefinito è [None](../revisiontexteffect/) |
| [get_RevisionBarsColor](./get_revisionbarscolor/)() const | Consente di specificare il colore da utilizzare per le barre laterali che identificano le righe del documento contenenti informazioni revisionate. Il valore predefinito è [Red](../revisioncolor/). |
| [get_RevisionBarsPosition](./get_revisionbarsposition/)() const | Ottiene o imposta la posizione di rendering delle barre di revisione. Il valore predefinito è [Outside](../../aspose.words.drawing/horizontalalignment/). |
| [get_RevisionBarsWidth](./get_revisionbarswidth/)() const | Ottiene o imposta la larghezza delle barre di revisione, punti. |
| [get_ShowInBalloons](./get_showinballoons/)() const | Consente di specificare se le revisioni vengono visualizzate nei balloon. Il valore predefinito è [None](../showinballoons/). |
| [get_ShowOriginalRevision](./get_showoriginalrevision/)() const | Consente di specificare se il testo originale deve essere mostrato al posto di quello revisionato. Il valore predefinito è **false**. |
| [get_ShowRevisionBars](./get_showrevisionbars/)() const | Consente di specificare se le barre di revisione devono essere visualizzate vicino alle righe contenenti contenuto revisionato. Il valore predefinito è **true**. |
| [get_ShowRevisionMarks](./get_showrevisionmarks/)() const | Consente di specificare se il testo della revisione deve essere contrassegnato con una formattazione speciale. Il valore predefinito è **true**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CommentColor](./set_commentcolor/)(Aspose::Words::Layout::RevisionColor) | Setter per [Aspose::Words::Layout::RevisionOptions::get_CommentColor](./get_commentcolor/). |
| [set_DeleteCellColor](./set_deletecellcolor/)(Aspose::Words::Layout::RevisionColor) | Impostatore per [Aspose::Words::Layout::RevisionOptions::get_DeleteCellColor](./get_deletecellcolor/). |
| [set_DeletedTextColor](./set_deletedtextcolor/)(Aspose::Words::Layout::RevisionColor) | Impostatore per [Aspose::Words::Layout::RevisionOptions::get_DeletedTextColor](./get_deletedtextcolor/). |
| [set_DeletedTextEffect](./set_deletedtexteffect/)(Aspose::Words::Layout::RevisionTextEffect) | Impostatore per [Aspose::Words::Layout::RevisionOptions::get_DeletedTextEffect](./get_deletedtexteffect/). |
| [set_InsertCellColor](./set_insertcellcolor/)(Aspose::Words::Layout::RevisionColor) | Impostatore per [Aspose::Words::Layout::RevisionOptions::get_InsertCellColor](./get_insertcellcolor/). |
| [set_InsertedTextColor](./set_insertedtextcolor/)(Aspose::Words::Layout::RevisionColor) | Impostatore per [Aspose::Words::Layout::RevisionOptions::get_InsertedTextColor](./get_insertedtextcolor/). |
| [set_InsertedTextEffect](./set_insertedtexteffect/)(Aspose::Words::Layout::RevisionTextEffect) | Impostatore per [Aspose::Words::Layout::RevisionOptions::get_InsertedTextEffect](./get_insertedtexteffect/). |
| [set_MeasurementUnit](./set_measurementunit/)(Aspose::Words::MeasurementUnits) | Consente di specificare le unità di misura per i commenti di revisione. Il valore predefinito è [Centimeters](../../aspose.words/measurementunits/) |
| [set_MovedFromTextColor](./set_movedfromtextcolor/)(Aspose::Words::Layout::RevisionColor) | Impostatore per [Aspose::Words::Layout::RevisionOptions::get_MovedFromTextColor](./get_movedfromtextcolor/). |
| [set_MovedFromTextEffect](./set_movedfromtexteffect/)(Aspose::Words::Layout::RevisionTextEffect) | Impostatore per [Aspose::Words::Layout::RevisionOptions::get_MovedFromTextEffect](./get_movedfromtexteffect/). |
| [set_MovedToTextColor](./set_movedtotextcolor/)(Aspose::Words::Layout::RevisionColor) | Impostatore per [Aspose::Words::Layout::RevisionOptions::get_MovedToTextColor](./get_movedtotextcolor/). |
| [set_MovedToTextEffect](./set_movedtotexteffect/)(Aspose::Words::Layout::RevisionTextEffect) | Impostatore per [Aspose::Words::Layout::RevisionOptions::get_MovedToTextEffect](./get_movedtotexteffect/). |
| [set_RevisedPropertiesColor](./set_revisedpropertiescolor/)(Aspose::Words::Layout::RevisionColor) | Impostatore per [Aspose::Words::Layout::RevisionOptions::get_RevisedPropertiesColor](./get_revisedpropertiescolor/). |
| [set_RevisedPropertiesEffect](./set_revisedpropertieseffect/)(Aspose::Words::Layout::RevisionTextEffect) | Impostatore per [Aspose::Words::Layout::RevisionOptions::get_RevisedPropertiesEffect](./get_revisedpropertieseffect/). |
| [set_RevisionBarsColor](./set_revisionbarscolor/)(Aspose::Words::Layout::RevisionColor) | Impostatore per [Aspose::Words::Layout::RevisionOptions::get_RevisionBarsColor](./get_revisionbarscolor/). |
| [set_RevisionBarsPosition](./set_revisionbarsposition/)(Aspose::Words::Drawing::HorizontalAlignment) | Impostatore per [Aspose::Words::Layout::RevisionOptions::get_RevisionBarsPosition](./get_revisionbarsposition/). |
| [set_RevisionBarsWidth](./set_revisionbarswidth/)(float) | Impostatore per [Aspose::Words::Layout::RevisionOptions::get_RevisionBarsWidth](./get_revisionbarswidth/). |
| [set_ShowInBalloons](./set_showinballoons/)(Aspose::Words::Layout::ShowInBalloons) | Impostatore per [Aspose::Words::Layout::RevisionOptions::get_ShowInBalloons](./get_showinballoons/). |
| [set_ShowOriginalRevision](./set_showoriginalrevision/)(bool) | Impostatore per [Aspose::Words::Layout::RevisionOptions::get_ShowOriginalRevision](./get_showoriginalrevision/). |
| [set_ShowRevisionBars](./set_showrevisionbars/)(bool) | Impostatore per [Aspose::Words::Layout::RevisionOptions::get_ShowRevisionBars](./get_showrevisionbars/). |
| [set_ShowRevisionMarks](./set_showrevisionmarks/)(bool) | Impostatore per [Aspose::Words::Layout::RevisionOptions::get_ShowRevisionMarks](./get_showrevisionmarks/). |
| static [Type](./type/)() |  |

## Esempi



Mostra come modificare l'aspetto delle revisioni in un documento di output renderizzato.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci una revisione, quindi cambia il colore di tutte le revisioni in verde.
builder->Writeln(u"This is not a revision.");
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
builder->Writeln(u"This is a revision.");
doc->StopTrackRevisions();
builder->Writeln(u"This is not a revision.");

// Rimuovi la barra che appare a sinistra di ogni riga revisionata.
doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertedTextColor(Aspose::Words::Layout::RevisionColor::BrightGreen);
doc->get_LayoutOptions()->get_RevisionOptions()->set_ShowRevisionBars(false);
doc->get_LayoutOptions()->get_RevisionOptions()->set_RevisionBarsPosition(Aspose::Words::Drawing::HorizontalAlignment::Right);

doc->Save(get_ArtifactsDir() + u"Revision.LayoutOptionsRevisions.pdf");
```

## Vedi anche

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
