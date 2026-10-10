---
title: "Aspose::Words::Saving::MultiPageLayout class"
linktitle: "MultiPageLayout"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::MultiPageLayout class. Definisce un layout per il rendering di più pagine in un unico output in C++."
type: docs
weight: 14500
url: /it/cpp/aspose.words.saving/multipagelayout/
---
## MultiPageLayout class


Definisce un layout per il rendering di più pagine in un unico output.

```cpp
class MultiPageLayout : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_BackColor](./get_backcolor/)() | Ottiene il colore di sfondo dell'output. Il valore predefinito è **Empty**. |
| [get_BorderColor](./get_bordercolor/)() | Ottiene il colore del bordo delle pagine. Il valore predefinito è **Empty**. |
| [get_BorderWidth](./get_borderwidth/)() const | Ottiene la larghezza del bordo delle pagine. Il valore predefinito è 0. |
| [GetType](./gettype/)() const override |  |
| static [Grid](./grid/)(int32_t, float, float) | Crea un layout in cui le pagine sono renderizzate da sinistra a destra, dall'alto verso il basso, in una griglia con il numero specificato di colonne. |
| static [Horizontal](./horizontal/)(float) | Crea un layout in cui tutte le pagine specificate sono renderizzate orizzontalmente affiancate, da sinistra a destra, in un unico output. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BackColor](./set_backcolor/)(System::Drawing::Color) | Imposta il colore di sfondo dell'output. Il valore predefinito è **Empty**. |
| [set_BorderColor](./set_bordercolor/)(System::Drawing::Color) | Imposta il colore del bordo delle pagine. Il valore predefinito è **Empty**. |
| [set_BorderWidth](./set_borderwidth/)(float) | Imposta la larghezza del bordo delle pagine. Il valore predefinito è 0. |
| static [SinglePage](./singlepage/)() | Crea un layout che renderizza solo la prima delle pagine specificate. |
| static [TiffFrames](./tiffframes/)() | Crea un layout in cui ogni pagina è renderizzata come un frame separato in un'immagine TIFF multi-frame. Applicabile solo ai formati immagine TIFF. |
| static [Type](./type/)() |  |
| static [Vertical](./vertical/)(float) | Crea un layout in cui tutte le pagine specificate vengono renderizzate verticalmente una sotto l'altra in un unico output. |

## Esempi



Mostra come salvare il documento in un'immagine JPG con le impostazioni di layout multipagina.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// Configura un layout a griglia con:
// - 3 colonne per riga.
// - Spaziatura di 10pt tra le pagine (orizzontale e verticale).
options->set_PageLayout(Aspose::Words::Saving::MultiPageLayout::Grid(3, 10.0f, 10.0f));

// Layout alternativi:
// options.PageLayout = MultiPageLayout.Horizontal(10);
// options.PageLayout = MultiPageLayout.Vertical(10);

// Personalizza lo sfondo e il bordo.
options->get_PageLayout()->set_BackColor(System::Drawing::Color::get_LightGray());
options->get_PageLayout()->set_BorderColor(System::Drawing::Color::get_Blue());
options->get_PageLayout()->set_BorderWidth(2.0f);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.GridLayout.jpg", options);
```

## Vedi anche

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
