---
title: "Aspose::Words::Shading class"
linktitle: "Ombreggiatura"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Shading class. Contiene gli attributi di ombreggiatura per un oggetto. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 60000
url: /it/cpp/aspose.words/shading/
---
## Shading class


Contiene attributi di ombreggiatura per un oggetto. Per saperne di più, visita l'articolo di documentazione [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class Shading : public Aspose::Words::InternableComplexAttr,
                public Aspose::Words::IComplexAttr
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Rimuove l'ombreggiatura dall'oggetto. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Shading\>\&) | Determina se il [Shading](./) specificato è uguale in valore al corrente [Shading](./). |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Determina se l'oggetto specificato è uguale in valore all'oggetto corrente. |
| [get_BackgroundPatternColor](./get_backgroundpatterncolor/)() | Ottiene o imposta il colore applicato allo sfondo dell'oggetto [Shading](./). |
| [get_BackgroundPatternThemeColor](./get_backgroundpatternthemecolor/)() | Ottiene o imposta il colore tematico del motivo di sfondo nello schema di colori applicato associato a questo oggetto [Shading](./). |
| [get_BackgroundTintAndShade](./get_backgroundtintandshade/)() | Ottiene o imposta un valore double che schiarisce o scurisce un colore tematico di sfondo. |
| [get_ForegroundPatternColor](./get_foregroundpatterncolor/)() | Ottiene o imposta il colore applicato al primo piano dell'oggetto [Shading](./). |
| [get_ForegroundPatternThemeColor](./get_foregroundpatternthemecolor/)() | Ottiene o imposta il colore tematico del motivo di primo piano nello schema colori applicato associato a questo oggetto [Shading](./). |
| [get_ForegroundTintAndShade](./get_foregroundtintandshade/)() | Ottiene o imposta un valore double che schiarisce o scurisce un colore tematico di primo piano. |
| [get_Texture](./get_texture/)() | Ottiene o imposta la texture dell'ombreggiatura. |
| [GetHashCode](./gethashcode/)() const override | Funziona come funzione hash per questo tipo. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BackgroundPatternColor](./set_backgroundpatterncolor/)(System::Drawing::Color) | Impostatore per [Aspose::Words::Shading::get_BackgroundPatternColor](./get_backgroundpatterncolor/). |
| [set_BackgroundPatternThemeColor](./set_backgroundpatternthemecolor/)(Aspose::Words::Themes::ThemeColor) | Impostatore per [Aspose::Words::Shading::get_BackgroundPatternThemeColor](./get_backgroundpatternthemecolor/). |
| [set_BackgroundTintAndShade](./set_backgroundtintandshade/)(double) | Impostatore per [Aspose::Words::Shading::get_BackgroundTintAndShade](./get_backgroundtintandshade/). |
| [set_ForegroundPatternColor](./set_foregroundpatterncolor/)(System::Drawing::Color) | Impostatore per [Aspose::Words::Shading::get_ForegroundPatternColor](./get_foregroundpatterncolor/). |
| [set_ForegroundPatternThemeColor](./set_foregroundpatternthemecolor/)(Aspose::Words::Themes::ThemeColor) | Impostatore per [Aspose::Words::Shading::get_ForegroundPatternThemeColor](./get_foregroundpatternthemecolor/). |
| [set_ForegroundTintAndShade](./set_foregroundtintandshade/)(double) | Impostatore per [Aspose::Words::Shading::get_ForegroundTintAndShade](./get_foregroundtintandshade/). |
| [set_Texture](./set_texture/)(Aspose::Words::TextureIndex) | Impostatore per [Aspose::Words::Shading::get_Texture](./get_texture/). |
| static [Type](./type/)() |  |

## Esempi



Mostra come applicare il colore del bordo e dell'ombreggiatura durante la creazione di una tabella.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Avvia una tabella e imposta un colore/spessore predefinito per i suoi bordi.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
table->SetBorders(Aspose::Words::LineStyle::Single, 2.0, System::Drawing::Color::get_Black());

// Crea una riga con due celle con colori di sfondo diversi.
builder->InsertCell();
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightSkyBlue());
builder->Writeln(u"Row 1, Cell 1.");
builder->InsertCell();
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_Orange());
builder->Writeln(u"Row 1, Cell 2.");
builder->EndRow();

// Reimposta la formattazione delle celle per disabilitare i colori di sfondo
// imposta uno spessore del bordo personalizzato per tutte le nuove celle create dal builder,
// quindi crea una seconda riga.
builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->get_Borders()->get_Left()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Right()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Top()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Bottom()->set_LineWidth(4.0);

builder->InsertCell();
builder->Writeln(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Writeln(u"Row 2, Cell 2.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.TableBordersAndShading.docx");
```


Mostra come decorare il testo con bordi e ombreggiatura.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::BorderCollection> borders = builder->get_ParagraphFormat()->get_Borders();
borders->set_DistanceFromText(20);
borders->idx_get(Aspose::Words::BorderType::Left)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Right)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Top)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Bottom)->set_LineStyle(Aspose::Words::LineStyle::Double);

System::SharedPtr<Aspose::Words::Shading> shading = builder->get_ParagraphFormat()->get_Shading();
shading->set_Texture(Aspose::Words::TextureIndex::TextureDiagonalCross);
shading->set_BackgroundPatternColor(System::Drawing::Color::get_LightCoral());
shading->set_ForegroundPatternColor(System::Drawing::Color::get_LightSalmon());

builder->Write(u"This paragraph is formatted with a double border and shading.");
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.ApplyBordersAndShading.docx");
```

## Vedi anche

* Class [InternableComplexAttr](../internablecomplexattr/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
