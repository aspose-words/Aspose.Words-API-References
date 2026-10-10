---
title: "Aspose::Words::Document::get_ViewOptions metodo"
linktitle: "get_ViewOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Document::get_ViewOptions metodo. Fornisce opzioni per controllare come il documento viene visualizzato in Microsoft Word in C++."
type: docs
weight: 58000
url: /it/cpp/aspose.words/document/get_viewoptions/
---
## Document::get_ViewOptions method


Fornisce opzioni per controllare come il documento viene visualizzato in Microsoft Word.

```cpp
System::SharedPtr<Aspose::Words::Settings::ViewOptions> Aspose::Words::Document::get_ViewOptions()
```


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


Mostra come impostare un tipo di zoom personalizzato, che le versioni più vecchie di Microsoft Word applicheranno a un documento al caricamento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Imposta la proprietà "ZoomType" su "ZoomType.PageWidth" per ottenere Microsoft Word
// per ingrandire automaticamente il documento in modo da adattarlo alla larghezza della pagina.
// Imposta la proprietà "ZoomType" su "ZoomType.FullPage" per ottenere Microsoft Word
// per ingrandire automaticamente il documento in modo da rendere visibile l'intera prima pagina.
// Imposta la proprietà "ZoomType" su "ZoomType.TextFit" per ottenere Microsoft Word
// per ingrandire automaticamente il documento in modo da adattarlo ai margini interni del testo della prima pagina.
doc->get_ViewOptions()->set_ZoomType(zoomType);

doc->Save(get_ArtifactsDir() + u"ViewOptions.SetZoomType.doc");
```

## Vedi anche

* Class [ViewOptions](../../../aspose.words.settings/viewoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
