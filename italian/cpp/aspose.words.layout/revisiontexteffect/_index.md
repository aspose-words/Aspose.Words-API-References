---
title: "Aspose::Words::Layout::RevisionTextEffect enum"
linktitle: "RevisionTextEffect"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Layout::RevisionTextEffect enum. Consente di specificare l'effetto di decorazione per le revisioni del testo del documento in C++."
type: docs
weight: 12000
url: /it/cpp/aspose.words.layout/revisiontexteffect/
---
## RevisionTextEffect enum


Consente di specificare l'effetto di decorazione per le revisioni del testo del documento.

```cpp
enum class RevisionTextEffect
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | 0 | Il contenuto revisionato non ha effetti speciali applicati. Questo corrisponde a [NoHighlight](../revisioncolor/). |
| Colore | 1 | Il contenuto revisionato è evidenziato solo con colore. |
| Grassetto | 2 | Il contenuto revisionato è reso in grassetto e colorato. |
| Corsivo | 3 | Il contenuto revisionato è reso in corsivo e colorato. |
| Sottolineatura | 4 | Il contenuto revisionato è sottolineato e colorato. |
| DoppiaSottolineatura | 5 | Il contenuto revisionato è doppio sottolineato e colorato. |
| Barrato | 6 | Il contenuto revisionato è barrato e colorato. |
| DoppioBarrato | 7 | Il contenuto revisionato è doppio barrato e colorato. |
| Nascosto | 8 | Il contenuto revisionato è nascosto. |


## Esempi



Mostra come modificare l'aspetto delle revisioni.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

// Ottieni l'oggetto RevisionOptions che controlla l'aspetto delle revisioni.
System::SharedPtr<Aspose::Words::Layout::RevisionOptions> revisionOptions = doc->get_LayoutOptions()->get_RevisionOptions();

// Visualizza le revisioni di inserimento in verde e corsivo.
revisionOptions->set_InsertedTextColor(Aspose::Words::Layout::RevisionColor::Green);
revisionOptions->set_InsertedTextEffect(Aspose::Words::Layout::RevisionTextEffect::Italic);

// Visualizza le revisioni di eliminazione in rosso e grassetto.
revisionOptions->set_DeletedTextColor(Aspose::Words::Layout::RevisionColor::Red);
revisionOptions->set_DeletedTextEffect(Aspose::Words::Layout::RevisionTextEffect::Bold);

// Lo stesso testo apparirà due volte in una revisione di spostamento:
// una volta al punto di partenza e una volta alla destinazione di arrivo.
// Visualizza il testo nella revisione di partenza in giallo con doppio barrato
// e in blu doppio sottolineato nella revisione di destinazione.
revisionOptions->set_MovedFromTextColor(Aspose::Words::Layout::RevisionColor::Yellow);
revisionOptions->set_MovedFromTextEffect(Aspose::Words::Layout::RevisionTextEffect::DoubleStrikeThrough);
revisionOptions->set_MovedToTextColor(Aspose::Words::Layout::RevisionColor::ClassicBlue);
revisionOptions->set_MovedToTextEffect(Aspose::Words::Layout::RevisionTextEffect::DoubleUnderline);

// Visualizza le revisioni di formattazione in rosso scuro e grassetto.
revisionOptions->set_RevisedPropertiesColor(Aspose::Words::Layout::RevisionColor::DarkRed);
revisionOptions->set_RevisedPropertiesEffect(Aspose::Words::Layout::RevisionTextEffect::Bold);

// Posiziona una barra spessa blu scuro sul lato sinistro della pagina accanto alle linee interessate dalle revisioni.
revisionOptions->set_RevisionBarsColor(Aspose::Words::Layout::RevisionColor::DarkBlue);
revisionOptions->set_RevisionBarsWidth(15.0f);

// Mostra i segni di revisione e il testo originale.
revisionOptions->set_ShowOriginalRevision(true);
revisionOptions->set_ShowRevisionMarks(true);

// Ottieni revisioni di spostamento, eliminazione, formattazione e commenti per farli apparire in palloncini verdi
// sul lato destro della pagina.
revisionOptions->set_ShowInBalloons(Aspose::Words::Layout::ShowInBalloons::Format);
revisionOptions->set_CommentColor(Aspose::Words::Layout::RevisionColor::BrightGreen);

// Queste funzionalità sono applicabili solo a formati come .pdf o .jpg.
doc->Save(get_ArtifactsDir() + u"Revision.RevisionOptions.pdf");
```

## Vedi anche

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
