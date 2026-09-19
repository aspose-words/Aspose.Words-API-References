---
title: "Aspose::Words::Drawing::PatternType enum"
linktitle: "PatternType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::PatternType enum. Specifica il modello di riempimento da utilizzare per riempire una forma in C++."
type: docs
weight: 31000
url: /it/cpp/aspose.words.drawing/patterntype/
---
## PatternType enum


Specifica il modello di riempimento da utilizzare per riempire una forma.

```cpp
enum class PatternType
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | -1 | Nessun modello. |
| Percent10 | 1 | 10% del colore di primo piano. |
| Percent20 | 2 | 20% del colore di primo piano. |
| Percent25 | 3 | 25% del colore di primo piano. |
| Percent30 | 4 | 30% del colore di primo piano. |
| Percent40 | 5 | 40% del colore di primo piano |
| Percent50 | 6 | 50% del colore di primo piano |
| Percent5 | 7 | 5% del colore di primo piano. |
| Percent60 | 8 | 60% del colore di primo piano. |
| Percent70 | 9 | 70% del colore di primo piano. |
| Percent75 | 10 | 75% del colore di primo piano. |
| Percent80 | 11 | 80% del colore di primo piano. |
| Percent90 | 12 | 90% del colore di primo piano. |
| Croce | 13 | Croce. |
| DarkDownwardDiagonal | 14 | Diagonale discendente scura. |
| DarkHorizontal | 15 | Orizzontale scuro. |
| DarkUpwardDiagonal | 16 | Diagonale ascendente scura. |
| DarkVertical | 17 | Verticale scuro. |
| DashedDownwardDiagonal | 18 | Diagonale discendente tratteggiata. |
| DashedHorizontal | 19 | Orizzontale tratteggiata. |
| DashedUpwardDiagonal | 20 | Diagonale ascendente tratteggiata. |
| DashedVertical | 21 | Verticale tratteggiata. |
| DiagonalBrick | 22 | Mattone diagonale. |
| DiagonalCross | 23 | Croce diagonale. |
| Divot | 24 | Divot del modello. |
| DottedDiamond | 25 | Diamante punteggiato. |
| DottedGrid | 26 | Griglia puntinata. |
| DownwardDiagonal | 27 | Diagonale discendente. |
| Orizzontale | 28 | Orizzontale. |
| HorizontalBrick | 29 | Mattone orizzontale. |
| LargeCheckerBoard | 30 | Grande scacchiera. |
| LargeConfetti | 31 | Grande confetti. |
| LargeGrid | 32 | Grande griglia. |
| LightDownwardDiagonal | 33 | Diagonale discendente leggera. |
| LightHorizontal | 34 | Orizzontale leggera. |
| LightUpwardDiagonal | 36 | Diagonale ascendente leggera. |
| LightVertical | 37 | Verticale leggera. |
| NarrowHorizontal | 38 | Orizzontale stretta. |
| NarrowVertical | 39 | Verticale stretta. |
| OutlinedDiamond | 40 | Diamante contornato. |
| Quadri | 41 | Quadri. |
| Scaglie | 42 | Scaglie. |
| SmallCheckerBoard | 43 | Scacchiera piccola. |
| SmallConfetti | 44 | Confetti piccoli. |
| SmallGrid | 45 | Griglia piccola. |
| SolidDiamond | 46 | Diamante pieno. |
| Sfera | 47 | Sfera. |
| Grata | 48 | Grata. |
| UpwardDiagonal | 49 | Diagonale verso l'alto. |
| Verticale | 50 | Verticale. |
| Wave | 51 | Onda. |
| Intreccio | 52 | Intreccio. |
| WideDownwardDiagonal | 53 | Diagonale discendente ampia. |
| WideUpwardDiagonal | 54 | Diagonale larga verso l'alto. |
| ZigZag | 55 | Zig zag. |


## Esempi



Mostra come impostare il modello per una forma.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape stroke pattern border.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Fill> fill = shape->get_Fill();

std::cout << System::String::Format(u"Pattern value is: {0}", fill->get_Pattern()) << std::endl;

// Esistono diversi modi per specificare il riempimento con un modello.
// 1 -  Applica il modello al riempimento della forma:
fill->Patterned(Aspose::Words::Drawing::PatternType::DiagonalBrick);

// 2 -  Applica il modello con colori di primo piano e di sfondo al riempimento della forma:
fill->Patterned(Aspose::Words::Drawing::PatternType::DiagonalBrick, System::Drawing::Color::get_Aqua(), System::Drawing::Color::get_Bisque());

doc->Save(get_ArtifactsDir() + u"Shape.FillPattern.docx");
```

## Vedi anche

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
