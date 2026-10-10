---
title: "Aspose::Words::Settings::ZoomType enum"
linktitle: "ZoomType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Settings::ZoomType enum. Valori possibili per la dimensione con cui il documento appare sullo schermo in Microsoft Word in C++."
type: docs
weight: 22000
url: /it/cpp/aspose.words.settings/zoomtype/
---
## ZoomType enum


Valori possibili per la dimensione con cui il documento appare sullo schermo in Microsoft Word.

```cpp
enum class ZoomType
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Personalizzato | 0 | La percentuale di zoom è impostata esplicitamente. Non viene ricalcolata automaticamente quando le dimensioni del controllo cambiano. |
| None | n/a | Indica di utilizzare la percentuale di zoom esplicita. Uguale a [Custom](./). |
| FullPage | 1 | La percentuale di zoom viene ricalcolata automaticamente per adattarsi a una pagina intera. |
| PageWidth | 2 | La percentuale di zoom viene ricalcolata automaticamente per adattarsi alla larghezza della pagina. |
| TextFit | 3 | La percentuale di zoom viene ricalcolata automaticamente per adattarsi al testo. |


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
