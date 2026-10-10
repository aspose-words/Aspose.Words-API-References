---
title: "Enum Aspose::Words::Settings::ViewType"
linktitle: "ViewType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Enum Aspose::Words::Settings::ViewType. Valori possibili per la modalità di visualizzazione in Microsoft Word in C++."
type: docs
weight: 21000
url: /it/cpp/aspose.words.settings/viewtype/
---
## ViewType enum


Valori possibili per la modalità di visualizzazione in Microsoft Word.

```cpp
enum class ViewType
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | 0 | Il documento verrà visualizzato nella vista predefinita dell'applicazione. |
| Reading | 0 | Il documento verrà visualizzato nella vista predefinita dell'applicazione. |
| PageLayout | 1 | Il documento verrà aperto in una vista che mostra il documento così come verrà stampato. |
| Contorno | 3 | Il documento verrà visualizzato in una vista ottimizzata per la creazione di schemi o di documenti lunghi. |
| Normale | 4 | Il documento verrà visualizzato in una vista ottimizzata per la creazione di schemi o di documenti lunghi. |
| Web | 5 | Il documento verrà visualizzato in una vista che imita il modo in cui questo documento sarebbe mostrato in una pagina web. |


## Esempi



Mostra come impostare un fattore di zoom personalizzato, che le versioni più vecchie di Microsoft Word applicheranno a un documento al caricamento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->get_ViewOptions()->set_ViewType(Aspose::Words::Settings::ViewType::PageLayout);
doc->get_ViewOptions()->set_ZoomPercent(50);

ASSERT_EQ(Aspose::Words::Settings::ZoomType::Custom, doc->get_ViewOptions()->get_ZoomType());
ASSERT_EQ(Aspose::Words::Settings::ZoomType::None, doc->get_ViewOptions()->get_ZoomType());

doc->Save(get_ArtifactsDir() + u"ViewOptions.SetZoomPercentage.doc");
```

## Vedi anche

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
