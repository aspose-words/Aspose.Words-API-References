---
title: "Aspose::Words::Drawing::Charts::AxisBuiltInUnit enum"
linktitle: "AxisBuiltInUnit"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::AxisBuiltInUnit enum. Specifica le unità di visualizzazione per un asse in C++."
type: docs
weight: 20000
url: /it/cpp/aspose.words.drawing.charts/axisbuiltinunit/
---
## AxisBuiltInUnit enum


Specifica le unità di visualizzazione per un asse.

```cpp
enum class AxisBuiltInUnit
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | 0 | Specifica che i valori sul grafico devono essere visualizzati così come sono. |
| Personalizzato | 1 | Specifica che i valori sul grafico devono essere divisi per un divisore definito dall'utente. Questo valore non è supportato dai nuovi tipi di grafico di MS Office 2016. |
| Miliardi | 2 | Specifica che i valori sul grafico devono essere divisi per 1.000.000.000. |
| HundredMillions | 3 | Specifica che i valori sul grafico devono essere divisi per 100.000.000. |
| Hundreds | 4 | Specifica che i valori sul grafico devono essere divisi per 100. |
| HundredThousands | 5 | Specifica che i valori nel grafico devono essere divisi per 100.000. |
| Millions | 6 | Specifica che i valori nel grafico devono essere divisi per 1.000.000. |
| TenMillions | 7 | Specifica che i valori nel grafico devono essere divisi per 10.000.000. |
| TenThousands | 8 | Specifica che i valori nel grafico devono essere divisi per 10.000. |
| Thousands | 9 | Specifica che i valori nel grafico devono essere divisi per 1.000. |
| Trillions | 10 | Specifica che i valori nel grafico devono essere divisi per 1.000.000.000.0000. |
| Percentage | 11 | Specifica che i valori nel grafico devono essere divisi per 0,01. Questo valore è supportato solo dai nuovi tipi di grafico di MS Office 2016. |


## Esempi



Mostra come manipolare i segni di graduazione e i valori visualizzati di un asse del grafico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Scatter, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(1, chart->get_Series()->get_Count());
ASSERT_EQ(u"Y-Values", chart->get_Series()->idx_get(0)->get_Name());

// Imposta i segni di graduazione minori dell'asse Y in modo che puntino lontano dall'area del grafico,
// e i segni di graduazione maggiori per attraversare l'asse.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> axis = chart->get_AxisY();
axis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
axis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Outside);

// Imposta l'asse Y per mostrare un segno maggiore ogni 10 unità e un segno minore ogni 1 unità.
axis->set_MajorUnit(10);
axis->set_MinorUnit(1);

// Imposta i limiti dell'asse Y a -10 e 20.
// Questo asse Y ora visualizzerà 4 segni maggiori e 27 segni minori.
axis->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(-10.0));
axis->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(20.0));

// Per l'asse X, imposta i segni maggiori ogni 10 unità,
// ogni segno minore a 2,5 unità.
axis = chart->get_AxisX();
axis->set_MajorUnit(10);
axis->set_MinorUnit(2.5);

// Configura entrambi i tipi di segni di graduazione per apparire all'interno dell'area del grafico.
axis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);
axis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);

// Imposta i limiti dell'asse X in modo che l'asse X copra 5 segni maggiori e 12 segni minori.
axis->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(-10.0));
axis->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(30.0));
axis->get_TickLabels()->set_Alignment(Aspose::Words::ParagraphAlignment::Right);

ASSERT_EQ(1, axis->get_TickLabels()->get_Spacing());
ASPOSE_ASSERT_EQ(doc, axis->get_DisplayUnit()->get_Document());

// Imposta le etichette dei segni per visualizzare il loro valore in milioni.
axis->get_DisplayUnit()->set_Unit(Aspose::Words::Drawing::Charts::AxisBuiltInUnit::Millions);

// Possiamo impostare un valore più specifico con cui le etichette dei segni visualizzeranno i loro valori.
// Questa istruzione è equivalente a quella sopra.
axis->get_DisplayUnit()->set_CustomUnit(1000000);

doc->Save(get_ArtifactsDir() + u"Charts.AxisDisplayUnit.docx");
```

## Vedi anche

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
