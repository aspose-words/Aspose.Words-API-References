---
title: "Aspose::Words::Settings::ViewOptions::get_ZoomPercent method"
linktitle: "get_ZoomPercent"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Settings::ViewOptions::get_ZoomPercent method. Ottiene o imposta la percentuale con cui desideri visualizzare il tuo documento in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.settings/viewoptions/get_zoompercent/
---
## ViewOptions::get_ZoomPercent method


Ottiene o imposta la percentuale con cui desideri visualizzare il tuo documento.

```cpp
int32_t Aspose::Words::Settings::ViewOptions::get_ZoomPercent() const
```

## Note


Sebbene Aspose.Words sia in grado di leggere e scrivere questa opzione, il suo utilizzo è specifico dell'applicazione. Ad esempio, MS Word 2013 non rispetta il valore di questa opzione.

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

* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
