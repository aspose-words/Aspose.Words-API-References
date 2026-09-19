---
title: "Aspose::Words::Drawing::Fill classe"
linktitle: "Riempimento"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Drawing::Fill. Rappresenta la formattazione di riempimento per un oggetto. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 1000
url: /it/cpp/aspose.words.drawing/fill/
---
## Fill class


Rappresenta la formattazione di riempimento per un oggetto. Per saperne di più, visita l'articolo di documentazione [Working with Graphic Elements](https://docs.aspose.com/words/cpp/working-with-graphic-elements/).

```cpp
class Fill : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_BackColor](./get_backcolor/)() | Ottiene o imposta un oggetto Color che rappresenta il colore di sfondo per il riempimento. |
| [get_BackThemeColor](./get_backthemecolor/)() | Ottiene o imposta un oggetto ThemeColor che rappresenta il colore di sfondo per il riempimento. |
| [get_BackTintAndShade](./get_backtintandshade/)() | Ottiene o imposta un valore double che schiarisce o scurisce il colore di sfondo. |
| [get_BaseForeColor](./get_baseforecolor/)() | Ottiene un oggetto Color che rappresenta il colore di primo piano di base per il riempimento senza alcun modificatore. |
| [get_Color](./get_color/)() | Ottiene o imposta un oggetto Color che rappresenta il colore di primo piano per il riempimento. |
| [get_FillType](./get_filltype/)() | Ottiene un tipo di riempimento. |
| [get_ForeColor](./get_forecolor/)() | Ottiene un oggetto Color che rappresenta il colore di primo piano per il riempimento. |
| [get_ForeThemeColor](./get_forethemecolor/)() | Ottiene o imposta un oggetto ThemeColor che rappresenta il colore di primo piano per il riempimento. |
| [get_ForeTintAndShade](./get_foretintandshade/)() | Ottiene o imposta un valore double che schiarisce o scurisce il colore di primo piano. |
| [get_GradientAngle](./get_gradientangle/)() | Ottiene o imposta l'angolo del riempimento gradiente. |
| [get_GradientStops](./get_gradientstops/)() | Ottiene una collezione di oggetti [GradientStop](../gradientstop/) per il riempimento. |
| [get_GradientStyle](./get_gradientstyle/)() | Ottiene lo stile gradiente [GradientStyle](../gradientstyle/) per il riempimento. |
| [get_GradientVariant](./get_gradientvariant/)() | Ottiene la variante gradiente [GradientVariant](../gradientvariant/) per il riempimento. |
| [get_ImageBytes](./get_imagebytes/)() | Ottiene i byte grezzi della texture o del modello di riempimento. |
| [get_Opacity](./get_opacity/)() | Ottiene o imposta il grado di opacità del riempimento specificato come valore compreso tra 0.0 (trasparente) e 1.0 (opaco). |
| [get_Pattern](./get_pattern/)() | Ottiene un [PatternType](../patterntype/) per il riempimento. |
| [get_PresetTexture](./get_presettexture/)() | Ottiene una [PresetTexture](../presettexture/) per il riempimento. |
| [get_RotateWithObject](./get_rotatewithobject/)() | Ottiene se il riempimento ruota con l'oggetto specificato. |
| [get_TextureAlignment](./get_texturealignment/)() | Ottiene o imposta l'allineamento per il riempimento a piastrelle di texture. |
| [get_Transparency](./get_transparency/)() | Ottiene o imposta il grado di trasparenza del riempimento specificato come valore compreso tra 0.0 (opaco) e 1.0 (trasparente). |
| [get_Visible](./get_visible/)() | Ottiene il valore che è **true** se la formattazione applicata a questa istanza è visibile. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OneColorGradient](./onecolorgradient/)(Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant, double) | Imposta il riempimento specificato a un gradiente monocolore. |
| [OneColorGradient](./onecolorgradient/)(System::Drawing::Color, Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant, double) | Imposta il riempimento specificato a un gradiente monocolore usando il colore specificato. |
| [Patterned](./patterned/)(Aspose::Words::Drawing::PatternType) | Imposta il riempimento specificato a un modello. |
| [Patterned](./patterned/)(Aspose::Words::Drawing::PatternType, System::Drawing::Color, System::Drawing::Color) | Imposta il riempimento specificato a un modello. |
| [PresetTextured](./presettextured/)(Aspose::Words::Drawing::PresetTexture) | Imposta il riempimento su una texture predefinita. |
| [set_BackColor](./set_backcolor/)(System::Drawing::Color) | Impostatore per [Aspose::Words::Drawing::Fill::get_BackColor](./get_backcolor/). |
| [set_BackThemeColor](./set_backthemecolor/)(Aspose::Words::Themes::ThemeColor) | Impostatore per [Aspose::Words::Drawing::Fill::get_BackThemeColor](./get_backthemecolor/). |
| [set_BackTintAndShade](./set_backtintandshade/)(double) | Impostatore per [Aspose::Words::Drawing::Fill::get_BackTintAndShade](./get_backtintandshade/). |
| [set_Color](./set_color/)(System::Drawing::Color) | Impostatore per [Aspose::Words::Drawing::Fill::get_Color](./get_color/). |
| [set_ForeColor](./set_forecolor/)(System::Drawing::Color) | Imposta un oggetto Color che rappresenta il colore di primo piano per il riempimento. |
| [set_ForeThemeColor](./set_forethemecolor/)(Aspose::Words::Themes::ThemeColor) | Impostatore per [Aspose::Words::Drawing::Fill::get_ForeThemeColor](./get_forethemecolor/). |
| [set_ForeTintAndShade](./set_foretintandshade/)(double) | Impostatore per [Aspose::Words::Drawing::Fill::get_ForeTintAndShade](./get_foretintandshade/). |
| [set_GradientAngle](./set_gradientangle/)(double) | Impostatore per [Aspose::Words::Drawing::Fill::get_GradientAngle](./get_gradientangle/). |
| [set_Opacity](./set_opacity/)(double) | Impostatore per [Aspose::Words::Drawing::Fill::get_Opacity](./get_opacity/). |
| [set_RotateWithObject](./set_rotatewithobject/)(bool) | Imposta se il riempimento ruota con l'oggetto specificato. |
| [set_TextureAlignment](./set_texturealignment/)(Aspose::Words::Drawing::TextureAlignment) | Impostatore per [Aspose::Words::Drawing::Fill::get_TextureAlignment](./get_texturealignment/). |
| [set_Transparency](./set_transparency/)(double) | Impostatore per [Aspose::Words::Drawing::Fill::get_Transparency](./get_transparency/). |
| [set_Visible](./set_visible/)(bool) | Imposta il valore a **true** se la formattazione applicata a questa istanza è visibile. |
| [SetImage](./setimage/)(const System::String\&) | Cambia il tipo di riempimento in immagine singola. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&) | Cambia il tipo di riempimento in immagine singola. |
| [SetImage](./setimage/)(const System::ArrayPtr\<uint8_t\>\&) | Cambia il tipo di riempimento in immagine singola. |
| [Solid](./solid/)() | Imposta il riempimento su un colore uniforme. |
| [Solid](./solid/)(System::Drawing::Color) | Imposta il riempimento su un colore uniforme specificato. |
| [TwoColorGradient](./twocolorgradient/)(Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant) | Imposta il riempimento specificato su una sfumatura a due colori. |
| [TwoColorGradient](./twocolorgradient/)(System::Drawing::Color, System::Drawing::Color, Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant) | Imposta il riempimento specificato su una sfumatura a due colori. |
| static [Type](./type/)() |  |
## Note


Usa la proprietà [Fill](../shapebase/get_fill/) o [Fill](../../aspose.words/font/get_fill/) per accedere alle proprietà di riempimento di un oggetto. Non crei istanze della classe [Fill](./) direttamente.

## Esempi



Mostra come riempire una forma con un colore solido.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Scrivi del testo, quindi coprilo con una forma fluttuante.
builder->get_Font()->set_Size(32);
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::CloudCallout, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 25, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 25, 250, 150, Aspose::Words::Drawing::WrapType::None);

// Usa la proprietà "StrokeColor" per impostare il colore del contorno della forma.
shape->set_StrokeColor(System::Drawing::Color::get_CadetBlue());

// Usa la proprietà "FillColor" per impostare il colore dell'area interna della forma.
shape->set_FillColor(System::Drawing::Color::get_LightBlue());

// La proprietà "Opacity" determina quanto è trasparente il colore su una scala da 0 a 1,
// con 1 completamente opaco e 0 invisibile.
// Il riempimento della forma per impostazione predefinita è completamente opaco, quindi non possiamo vedere il testo su cui questa forma è sovrapposta.
ASPOSE_ASSERT_EQ(1.0, shape->get_Fill()->get_Opacity());

// Imposta l'opacità del colore di riempimento della forma a un valore più basso in modo da poter vedere il testo sottostante.
shape->get_Fill()->set_Opacity(0.3);

doc->Save(get_ArtifactsDir() + u"Shape.Fill.docx");
```

## Vedi anche

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
