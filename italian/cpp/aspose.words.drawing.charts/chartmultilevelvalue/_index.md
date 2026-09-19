---
title: "Aspose::Words::Drawing::Charts::ChartMultilevelValue class"
linktitle: "ChartMultilevelValue"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartMultilevelValue class. Rappresenta un valore per i grafici che visualizzano dati a più livelli in C++."
type: docs
weight: 14500
url: /it/cpp/aspose.words.drawing.charts/chartmultilevelvalue/
---
## ChartMultilevelValue class


Rappresenta un valore per i grafici che mostrano dati a più livelli.

```cpp
class ChartMultilevelValue : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [ChartMultilevelValue](./chartmultilevelvalue/)(const System::String\&, const System::String\&, const System::String\&) | Inizializza una nuova istanza di questa classe che rappresenta un valore a tre livelli. |
| [ChartMultilevelValue](./chartmultilevelvalue/)(const System::String\&, const System::String\&) | Inizializza una nuova istanza di questa classe che rappresenta un valore a due livelli. |
| [ChartMultilevelValue](./chartmultilevelvalue/)(const System::String\&) | Inizializza una nuova istanza di questa classe che rappresenta un valore a livello singolo. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Ottiene un flag che indica se l'oggetto specificato è uguale all'oggetto dati multilevel corrente. |
| [get_Level1](./get_level1/)() const | Ottiene il nome del livello superiore del grafico a cui si riferisce questo valore. |
| [get_Level2](./get_level2/)() const | Ottiene il nome del livello intermedio del grafico a cui si riferisce questo valore. |
| [get_Level3](./get_level3/)() const | Ottiene il nome del livello inferiore del grafico a cui si riferisce questo valore. |
| [GetHashCode](./gethashcode/)() const override | Ottiene un codice hash per l'oggetto dati multilevel corrente. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Esempi



Mostra come creare un grafico a mappa ad albero.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci un grafico a mappa ad albero.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Treemap, 450, 280);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
chart->get_Title()->set_Text(u"World Population");

// Elimina la serie generata di default.
chart->get_Series()->Clear();

// Aggiungi una serie.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Population by Region", System::MakeArray<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartMultilevelValue>>({System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"China"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"India"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Indonesia"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Pakistan"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Bangladesh"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Japan"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Philippines"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Africa", u"Nigeria"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Africa", u"Ethiopia"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Africa", u"Egypt"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Africa", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Europe", u"Russia"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Europe", u"Germany"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Europe", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Latin America", u"Brazil"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Latin America", u"Mexico"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Latin America", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Northern America", u"United States", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Northern America", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Oceania")}), System::MakeArray<double>({1409670000, 1400744000, 279118866, 241499431, 169828911, 123930000, 112892781, 764000000, 223800000, 107334000, 105914499, 903000000, 146150789, 84607016, 516000000, 203080756, 129713690, 310000000, 335893238, 35000000, 42000000}));

// Mostra le etichette dati.
series->set_HasDataLabels(true);
series->get_DataLabels()->set_ShowValue(true);
series->get_DataLabels()->set_ShowCategoryName(true);
System::String thousandSeparator = System::Globalization::CultureInfo::get_CurrentCulture()->get_NumberFormat()->get_CurrencyGroupSeparator();
series->get_DataLabels()->get_NumberFormat()->set_FormatCode(System::String::Format(u"#{0}0", thousandSeparator));

doc->Save(get_ArtifactsDir() + u"Charts.Treemap.docx");
```

## Vedi anche

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
