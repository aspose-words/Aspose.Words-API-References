---
title: "Aspose::Words::Drawing::Charts::AxisScaleType enum"
linktitle: "AxisScaleType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::AxisScaleType enum. Specifica i possibili tipi di scala per un asse in C++."
type: docs
weight: 23000
url: /it/cpp/aspose.words.drawing.charts/axisscaletype/
---
## AxisScaleType enum


Specifica i possibili tipi di scala per un asse.

```cpp
enum class AxisScaleType
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Lineare | 0 | Scalatura lineare. |
| Logaritmica | 1 | Scalatura logaritmica. |


## Esempi



Mostra come applicare la scalatura logaritmica a un asse del grafico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Scatter, 450, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// Cancella la serie di dati demo del grafico per iniziare con un grafico pulito.
chart->get_Series()->Clear();

// Inserisci una serie con coordinate X/Y per cinque punti.
chart->get_Series()->Add(u"Series 1", System::MakeArray<double>({1.0, 2.0, 3.0, 4.0, 5.0}), System::MakeArray<double>({1.0, 20.0, 400.0, 8000.0, 160000.0}));

// La scalatura dell'asse X è lineare per impostazione predefinita,
// mostrando valori incrementali uniformi che coprono il nostro intervallo di valori X (0, 1, 2, 3...).
// Un asse lineare non è ideale per i nostri valori Y
// poiché i punti con valori Y più piccoli saranno più difficili da leggere.
// Una scalatura logaritmica con base 20 (1, 20, 400, 8000...)
// distribuirà i punti tracciati, consentendoci di leggere più facilmente i loro valori sul grafico.
chart->get_AxisY()->get_Scaling()->set_Type(Aspose::Words::Drawing::Charts::AxisScaleType::Logarithmic);
chart->get_AxisY()->get_Scaling()->set_LogBase(20);

doc->Save(get_ArtifactsDir() + u"Charts.AxisScaling.docx");
```

## Vedi anche

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
