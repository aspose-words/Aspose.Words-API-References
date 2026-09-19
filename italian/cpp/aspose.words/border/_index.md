---
title: "classe Aspose::Words::Border"
linktitle: "Border"
second_title: "Riferimento API Aspose.Words per C++"
description: "classe Aspose::Words::Border. Rappresenta un bordo di un oggetto. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words/border/
---
## Border class


Rappresenta un bordo di un oggetto. Per saperne di più, visita l'articolo di documentazione [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class Border : public Aspose::Words::InternableComplexAttr,
               public Aspose::Words::IComplexAttr
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Reimposta le proprietà del bordo ai valori predefiniti. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Border\>\&) | Determina se il bordo specificato è uguale in valore al bordo corrente. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Determina se l'oggetto specificato è uguale in valore all'oggetto corrente. |
| [get_Color](./get_color/)() | Ottiene o imposta il colore del bordo. |
| [get_DistanceFromText](./get_distancefromtext/)() | Ottiene o imposta la distanza del bordo dal testo o dal bordo della pagina in punti. |
| [get_IsVisible](./get_isvisible/)() | Restituisce **true** se il [LineStyle](./get_linestyle/) non è [None](../linestyle/). |
| [get_LineStyle](./get_linestyle/)() | Ottiene o imposta lo stile del bordo. |
| [get_LineWidth](./get_linewidth/)() | Ottiene o imposta la larghezza del bordo in punti. |
| [get_Shadow](./get_shadow/)() | Ottiene o imposta un valore che indica se il bordo ha un'ombra. |
| [get_ThemeColor](./get_themecolor/)() | Ottiene o imposta il colore del tema nello schema colore applicato associato a questo oggetto [Border](./). |
| [get_TintAndShade](./get_tintandshade/)() | Ottiene o imposta un valore double che schiarisce o scurisce un colore. |
| [GetHashCode](./gethashcode/)() const override | Funziona come funzione hash per questo tipo. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Color](./set_color/)(System::Drawing::Color) | Setter per [Aspose::Words::Border::get_Color](./get_color/). |
| [set_DistanceFromText](./set_distancefromtext/)(double) | Setter per [Aspose::Words::Border::get_DistanceFromText](./get_distancefromtext/). |
| [set_LineStyle](./set_linestyle/)(Aspose::Words::LineStyle) | Setter per [Aspose::Words::Border::get_LineStyle](./get_linestyle/). |
| [set_LineWidth](./set_linewidth/)(double) | Setter per [Aspose::Words::Border::get_LineWidth](./get_linewidth/). |
| [set_Shadow](./set_shadow/)(bool) | Setter per [Aspose::Words::Border::get_Shadow](./get_shadow/). |
| [set_ThemeColor](./set_themecolor/)(Aspose::Words::Themes::ThemeColor) | Impostatore per [Aspose::Words::Border::get_ThemeColor](./get_themecolor/). |
| [set_TintAndShade](./set_tintandshade/)(double) | Impostatore per [Aspose::Words::Border::get_TintAndShade](./get_tintandshade/). |
| static [Type](./type/)() |  |
## Note


I bordi possono essere applicati a vari elementi del documento, inclusi il paragrafo, la sequenza di testo all'interno di un paragrafo o una cella di tabella.

## Esempi



Mostra come inserire una stringa circondata da un bordo in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(get_ArtifactsDir() + u"Border.FontBorder.docx");
```


Mostra come inserire un paragrafo con un bordo superiore.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Border> topBorder = builder->get_ParagraphFormat()->get_Borders()->get_Top();
topBorder->set_LineWidth(4.0);
topBorder->set_LineStyle(Aspose::Words::LineStyle::DashSmallGap);
// Imposta ThemeColor solo quando LineWidth o LineStyle sono impostati.
topBorder->set_ThemeColor(Aspose::Words::Themes::ThemeColor::Accent1);
topBorder->set_TintAndShade(0.25);

builder->Writeln(u"Text with a top border.");

doc->Save(get_ArtifactsDir() + u"Border.ParagraphTopBorder.docx");
```

## Vedi anche

* Class [InternableComplexAttr](../internablecomplexattr/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
