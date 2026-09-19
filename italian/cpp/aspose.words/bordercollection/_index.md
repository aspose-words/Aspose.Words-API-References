---
title: "Aspose::Words::BorderCollection classe"
linktitle: "BorderCollection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::BorderCollection classe. Una raccolta di oggetti Border. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words/bordercollection/
---
## BorderCollection class


Una raccolta di oggetti [Border](../border/). Per saperne di più, visita l'articolo della documentazione [Programmazione con i Documenti](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class BorderCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Border>>
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Rimuove tutti i bordi di un oggetto. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::BorderCollection\>\&) | Confronta le raccolte di bordi. |
| [get_Bottom](./get_bottom/)() | Ottiene il bordo inferiore. |
| [get_Color](./get_color/)() | Ottiene o imposta il colore del bordo. |
| [get_Count](./get_count/)() | Ottiene il numero di bordi nella raccolta. |
| [get_DistanceFromText](./get_distancefromtext/)() | Ottiene o imposta la distanza del bordo dal testo in punti. |
| [get_Horizontal](./get_horizontal/)() | Ottiene il bordo orizzontale utilizzato tra le celle o i paragrafi corrispondenti. |
| [get_Left](./get_left/)() | Ottiene il bordo sinistro. |
| [get_LineStyle](./get_linestyle/)() | Ottiene o imposta lo stile del bordo. |
| [get_LineWidth](./get_linewidth/)() | Ottiene o imposta la larghezza del bordo in punti. |
| [get_Right](./get_right/)() | Ottiene il bordo destro. |
| [get_Shadow](./get_shadow/)() | Ottiene o imposta un valore che indica se il bordo ha un'ombra. |
| [get_Top](./get_top/)() | Ottiene il bordo superiore. |
| [get_Vertical](./get_vertical/)() | Ottiene il bordo verticale utilizzato tra le celle. |
| [GetEnumerator](./getenumerator/)() override | Restituisce un oggetto enumeratore che può essere usato per iterare su tutti i bordi nella raccolta. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(Aspose::Words::BorderType) | Recupera un oggetto [Border](../border/) per tipo di bordo. |
| [idx_get](./idx_get/)(int32_t) | Recupera un oggetto [Border](../border/) per indice. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Color](./set_color/)(System::Drawing::Color) | Metodo set per [Aspose::Words::BorderCollection::get_Color](./get_color/). |
| [set_DistanceFromText](./set_distancefromtext/)(double) | Metodo set per [Aspose::Words::BorderCollection::get_DistanceFromText](./get_distancefromtext/). |
| [set_LineStyle](./set_linestyle/)(Aspose::Words::LineStyle) | Metodo set per [Aspose::Words::BorderCollection::get_LineStyle](./get_linestyle/). |
| [set_LineWidth](./set_linewidth/)(double) | Metodo set per [Aspose::Words::BorderCollection::get_LineWidth](./get_linewidth/). |
| [set_Shadow](./set_shadow/)(bool) | Metodo setter per [Aspose::Words::BorderCollection::get_Shadow](./get_shadow/). |
| static [Type](./type/)() |  |

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
