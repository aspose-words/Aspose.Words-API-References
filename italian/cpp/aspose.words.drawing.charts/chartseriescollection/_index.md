---
title: "Aspose::Words::Drawing::Charts::ChartSeriesCollection classe"
linktitle: "ChartSeriesCollection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartSeriesCollection classe. Rappresenta una raccolta di un ChartSeries. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 17000
url: /it/cpp/aspose.words.drawing.charts/chartseriescollection/
---
## ChartSeriesCollection class


Rappresenta una raccolta di un [ChartSeries](../chartseries/). Per saperne di più, visita l'articolo di documentazione [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartSeriesCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries>>
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<double\>\&) | Aggiunge un nuovo [ChartSeries](../chartseries/) a questa raccolta. Usa questo metodo per aggiungere serie a qualsiasi tipo di grafico a barre, colonne, linee e superfici. |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<double\>\&, const System::ArrayPtr\<bool\>\&) |  |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<double\>\&, const System::ArrayPtr\<double\>\&) | Aggiunge un nuovo [ChartSeries](../chartseries/) a questa raccolta. Usa questo metodo per aggiungere serie a qualsiasi tipo di grafico a dispersione. |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<System::DateTime\>\&, const System::ArrayPtr\<double\>\&) | Aggiunge un nuovo [ChartSeries](../chartseries/) a questa raccolta. Usa questo metodo per aggiungere serie a qualsiasi tipo di grafico ad area, radar e azionario. |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<double\>\&, const System::ArrayPtr\<double\>\&, const System::ArrayPtr\<double\>\&) | Aggiunge un nuovo [ChartSeries](../chartseries/) a questa raccolta. Usa questo metodo per aggiungere serie a qualsiasi tipo di grafico a bolle. |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartMultilevelValue\>\>\&, const System::ArrayPtr\<double\>\&) | Aggiunge un nuovo [ChartSeries](../chartseries/) a questa raccolta. Usa questo metodo per aggiungere serie che hanno categorie di dati a più livelli. |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<double\>\&) | Aggiunge un nuovo [ChartSeries](../chartseries/) a questa raccolta. Usa questo metodo per aggiungere serie a grafici istogramma. |
| [Clear](./clear/)() | Rimuove tutti i [ChartSeries](../chartseries/) da questa raccolta. |
| [get_Count](./get_count/)() | Restituisce il numero di [ChartSeries](../chartseries/) in questa raccolta. |
| [GetEnumerator](./getenumerator/)() override | Restituisce un oggetto enumeratore. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Restituisce un [ChartSeries](../chartseries/) all'indice specificato. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [RemoveAt](./removeat/)(int32_t) | Rimuove un [ChartSeries](../chartseries/) all'indice specificato. |
| static [Type](./type/)() |  |

## Esempi



Mostra come aggiungere e rimuovere dati di serie in un grafico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci un grafico a colonne che conterrà tre serie di dati dimostrativi per impostazione predefinita.
System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 400, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// Ogni serie ha quattro valori decimali: uno per ciascuna delle quattro categorie.
// Quattro gruppi di tre colonne rappresenteranno questi dati.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> chartData = chart->get_Series();

ASSERT_EQ(3, chartData->get_Count());

// Stampa il nome di ogni serie nel grafico.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries>>> enumerator = chart->get_Series()->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << enumerator->get_Current()->get_Name() << std::endl;
    }
}

// Questi sono i nomi delle categorie nel grafico.
System::ArrayPtr<System::String> categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3", u"Category 4"});

// Possiamo aggiungere una serie con nuovi valori per le categorie esistenti.
// Questo grafico conterrà ora quattro gruppi di quattro colonne.
chart->get_Series()->Add(u"Series 4", categories, System::MakeArray<double>({4.4, 7.0, 3.5, 2.1}));

// Una serie del grafico può anche essere rimossa per indice, così.
// Questo rimuoverà una delle tre serie demo incluse nel grafico.
chartData->RemoveAt(2);

ASSERT_FALSE(chartData->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> s) -> bool
{
    return s->get_Name() == u"Series 3";
}))));

// Possiamo anche cancellare tutti i dati del grafico in una volta con questo metodo.
// Quando si crea un nuovo grafico, questo è il modo per cancellare tutti i dati demo
// prima di poter iniziare a lavorare su un grafico vuoto.
chartData->Clear();
```

## Vedi anche

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
