---
title: "Aspose::Words::BorderType enum"
linktitle: "BorderType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Enum Aspose::Words::BorderType. Specifica i lati di un bordo. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 81000
url: /it/cpp/aspose.words/bordertype/
---
## BorderType enum


Specifica i lati di un bordo. Per saperne di più, visita l'articolo di documentazione [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
enum class BorderType
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | -1 | Valore predefinito. |
| Inferiore | 0 | Specifica il bordo inferiore di un paragrafo o di una cella di tabella. |
| Sinistra | 1 | Specifica il bordo sinistro di un paragrafo o di una cella di tabella. |
| Destra | 2 | Specifica il bordo destro di un paragrafo o di una cella di tabella. |
| Superiore | 3 | Specifica il bordo superiore di un paragrafo o di una cella di tabella. |
| Orizzontale | 4 | Specifica il bordo orizzontale tra le celle di una tabella o tra paragrafi corrispondenti. |
| Verticale | 5 | Specifica il bordo verticale tra le celle di una tabella. |
| DiagonaleGiù | 6 | Specifica il bordo diagonale in una cella di tabella. |
| DiagonaleSu | 7 | Specifica il bordo diagonale in una cella di tabella. |


## Esempi



Mostra come inserire un paragrafo con un bordo superiore.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Border> topBorder = builder->get_ParagraphFormat()->get_Borders()->get_Top();
topBorder->set_LineWidth(4.0);
topBorder->set_LineStyle(Aspose::Words::LineStyle::DashSmallGap);
// Imposta ThemeColor solo quando LineWidth o LineStyle sono impostati.
topBorder->set_ThemeColor(Aspose::Words::Themes::ThemeColor::Accent1);
topBorder->set_TintAndShade(0.25);

builder->Writeln(u"Text with a top border.");

doc->Save(get_ArtifactsDir() + u"Border.ParagraphTopBorder.docx");
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
