---
title: "Aspose::Words::Layout::RevisionColor enum"
linktitle: "RevisionColor"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Layout::RevisionColor enum. Consente di specificare il colore delle revisioni del documento in C++."
type: docs
weight: 11000
url: /it/cpp/aspose.words.layout/revisioncolor/
---
## RevisionColor enum


Consente di specificare il colore delle revisioni del documento.

```cpp
enum class RevisionColor
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Auto | 0 | Predefinito. |
| Nero | 1 | Rappresenta il colore 000000. |
| Blu | 2 | Rappresenta il colore 2e97d3. |
| BrightGreen | 3 | Rappresenta il colore 84a35b. |
| ClassicBlue | 4 | Rappresenta il colore 0000ff. |
| ClassicRed | 5 | Rappresenta il colore ff0000. |
| DarkBlue | 6 | Rappresenta il colore 376e96. |
| DarkRed | 7 | Rappresenta il colore 881824. |
| DarkYellow | 8 | Rappresenta il colore e09a2b. |
| Gray25 | 9 | Rappresenta il colore a0a3a9. |
| Gray50 | 10 | Rappresenta il colore 50565e. |
| Green | 11 | Rappresenta il colore 2c6234. |
| Pink | 12 | Rappresenta il colore ce338f. |
| Red | 13 | Rappresenta il colore b5082e. |
| Teal | 14 | Rappresenta il colore 1b9cab. |
| Turquoise | 15 | Rappresenta il colore 3eafc2. |
| Violet | 16 | Rappresenta il colore 633277. |
| White | 17 | Rappresenta il colore ffffff. |
| Yellow | 18 | Rappresenta il colore fad272. |
| LightPink | 19 | Rappresenta il colore fce6f4. |
| LightBlue | 20 | Rappresenta il colore e1f2fa. |
| LightYellow | 21 | Rappresenta il colore fef4de. |
| ViolaChiaro | 22 | Rappresenta il colore eadfef. |
| ArancioneChiaro | 23 | Rappresenta il colore fce3d0. |
| VerdeChiaro | 24 | Rappresenta il colore e9f8ce. |
| Grigio | 25 | Rappresenta il colore efeded. |
| NessunaEvidenziazione | 26 | Nessun colore è usato per evidenziare le modifiche di revisione. |
| PerAutore | 27 | Le revisioni di ciascun autore ricevono un proprio colore per l'evidenziazione da un set predefinito di colori ad alto contrasto. |


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
