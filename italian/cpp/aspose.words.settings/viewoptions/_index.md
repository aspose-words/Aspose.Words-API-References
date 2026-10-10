---
title: "Classe Aspose::Words::Settings::ViewOptions"
linktitle: "ViewOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Settings::ViewOptions. Fornisce varie opzioni che controllano come un documento viene visualizzato in Microsoft Word. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words.settings/viewoptions/
---
## ViewOptions class


Fornisce varie opzioni che controllano come un documento viene visualizzato in Microsoft Word. Per saperne di più, visita l'articolo di documentazione [Lavorare con le opzioni e l'aspetto dei documenti Word](https://docs.aspose.com/words/cpp/work-with-word-document-options-and-appearance/).

```cpp
class ViewOptions : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_DisplayBackgroundShape](./get_displaybackgroundshape/)() const | Controlla la visualizzazione della forma di sfondo nella visualizzazione layout di stampa. |
| [get_DoNotDisplayPageBoundaries](./get_donotdisplaypageboundaries/)() const | Disattiva la visualizzazione dello spazio tra la parte superiore del testo e il bordo superiore della pagina. |
| [get_FormsDesign](./get_formsdesign/)() const | Specifica se il documento è in modalità di progettazione dei moduli. |
| [get_ViewType](./get_viewtype/)() const | Controlla la modalità di visualizzazione in Microsoft Word. |
| [get_ZoomPercent](./get_zoompercent/)() const | Ottiene o imposta la percentuale con cui desideri visualizzare il tuo documento. |
| [get_ZoomType](./get_zoomtype/)() const | Ottiene o imposta un valore di zoom basato sulla dimensione della finestra. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DisplayBackgroundShape](./set_displaybackgroundshape/)(bool) | Impostatore per [Aspose::Words::Settings::ViewOptions::get_DisplayBackgroundShape](./get_displaybackgroundshape/). |
| [set_DoNotDisplayPageBoundaries](./set_donotdisplaypageboundaries/)(bool) | Impostatore per [Aspose::Words::Settings::ViewOptions::get_DoNotDisplayPageBoundaries](./get_donotdisplaypageboundaries/). |
| [set_FormsDesign](./set_formsdesign/)(bool) | Impostatore per [Aspose::Words::Settings::ViewOptions::get_FormsDesign](./get_formsdesign/). |
| [set_ViewType](./set_viewtype/)(Aspose::Words::Settings::ViewType) | Impostatore per [Aspose::Words::Settings::ViewOptions::get_ViewType](./get_viewtype/). |
| [set_ZoomPercent](./set_zoompercent/)(int32_t) | Impostatore per [Aspose::Words::Settings::ViewOptions::get_ZoomPercent](./get_zoompercent/). |
| [set_ZoomType](./set_zoomtype/)(Aspose::Words::Settings::ZoomType) | Impostatore per [Aspose::Words::Settings::ViewOptions::get_ZoomType](./get_zoomtype/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
