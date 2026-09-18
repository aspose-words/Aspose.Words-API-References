---
title: "Aspose::Words::Drawing::Fill-Klasse"
linktitle: "Füllung"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Fill-Klasse. Stellt die Füllformatierung für ein Objekt dar. Weitere Informationen findest du im Dokumentationsartikel für C++."
type: docs
weight: 1000
url: /de/cpp/aspose.words.drawing/fill/
---
## Fill class


Stellt die Füllformatierung für ein Objekt dar. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Graphic Elements](https://docs.aspose.com/words/cpp/working-with-graphic-elements/).

```cpp
class Fill : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_BackColor](./get_backcolor/)() | Liest oder setzt ein Color-Objekt, das die Hintergrundfarbe der Füllung darstellt. |
| [get_BackThemeColor](./get_backthemecolor/)() | Liest oder legt ein ThemeColor-Objekt fest, das die Hintergrundfarbe für die Füllung darstellt. |
| [get_BackTintAndShade](./get_backtintandshade/)() | Liest oder legt einen double-Wert fest, der die Hintergrundfarbe aufhellt oder abdunkelt. |
| [get_BaseForeColor](./get_baseforecolor/)() | Liest ein Color-Objekt, das die Basis-Vordergrundfarbe für die Füllung ohne Modifikatoren darstellt. |
| [get_Color](./get_color/)() | Liest oder legt ein Color-Objekt fest, das die Vordergrundfarbe für die Füllung darstellt. |
| [get_FillType](./get_filltype/)() | Liest einen Fülltyp. |
| [get_ForeColor](./get_forecolor/)() | Liest ein Color-Objekt, das die Vordergrundfarbe für die Füllung darstellt. |
| [get_ForeThemeColor](./get_forethemecolor/)() | Liest oder legt ein ThemeColor-Objekt fest, das die Vordergrundfarbe für die Füllung darstellt. |
| [get_ForeTintAndShade](./get_foretintandshade/)() | Liest oder legt einen double-Wert fest, der die Vordergrundfarbe aufhellt oder abdunkelt. |
| [get_GradientAngle](./get_gradientangle/)() | Liest oder legt den Winkel der Farbverlauf-Füllung fest. |
| [get_GradientStops](./get_gradientstops/)() | Liest eine Sammlung von [GradientStop](../gradientstop/) Objekten für die Füllung. |
| [get_GradientStyle](./get_gradientstyle/)() | Liest den Farbverlauf-Stil [GradientStyle](../gradientstyle/) für die Füllung. |
| [get_GradientVariant](./get_gradientvariant/)() | Liest die Farbverlauf-Variante [GradientVariant](../gradientvariant/) für die Füllung. |
| [get_ImageBytes](./get_imagebytes/)() | Liest die Rohbytes der Fülltextur oder des Musters. |
| [get_Opacity](./get_opacity/)() | Liest oder legt den Grad der Deckkraft der angegebenen Füllung als Wert zwischen 0,0 (klar) und 1,0 (undurchsichtig) fest. |
| [get_Pattern](./get_pattern/)() | Liest einen [PatternType](../patterntype/) für die Füllung. |
| [get_PresetTexture](./get_presettexture/)() | Liest eine [PresetTexture](../presettexture/) für die Füllung. |
| [get_RotateWithObject](./get_rotatewithobject/)() | Liest, ob die Füllung mit dem angegebenen Objekt rotiert. |
| [get_TextureAlignment](./get_texturealignment/)() | Liest oder legt die Ausrichtung für Kacheltextur-Füllung fest. |
| [get_Transparency](./get_transparency/)() | Liest oder legt den Grad der Transparenz der angegebenen Füllung als Wert zwischen 0,0 (undurchsichtig) und 1,0 (klar) fest. |
| [get_Visible](./get_visible/)() | Liest den Wert, der **true** ist, wenn die auf diese Instanz angewendete Formatierung sichtbar ist. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OneColorGradient](./onecolorgradient/)(Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant, double) | Setzt die angegebene Füllung auf einen Einfarb-Farbverlauf. |
| [OneColorGradient](./onecolorgradient/)(System::Drawing::Color, Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant, double) | Setzt die angegebene Füllung auf einen Einfarb-Farbverlauf unter Verwendung der angegebenen Farbe. |
| [Patterned](./patterned/)(Aspose::Words::Drawing::PatternType) | Setzt die angegebene Füllung auf ein Muster. |
| [Patterned](./patterned/)(Aspose::Words::Drawing::PatternType, System::Drawing::Color, System::Drawing::Color) | Setzt die angegebene Füllung auf ein Muster. |
| [PresetTextured](./presettextured/)(Aspose::Words::Drawing::PresetTexture) | Setzt die Füllung auf eine voreingestellte Textur. |
| [set_BackColor](./set_backcolor/)(System::Drawing::Color) | Setter für [Aspose::Words::Drawing::Fill::get_BackColor](./get_backcolor/). |
| [set_BackThemeColor](./set_backthemecolor/)(Aspose::Words::Themes::ThemeColor) | Setter für [Aspose::Words::Drawing::Fill::get_BackThemeColor](./get_backthemecolor/). |
| [set_BackTintAndShade](./set_backtintandshade/)(double) | Setter für [Aspose::Words::Drawing::Fill::get_BackTintAndShade](./get_backtintandshade/). |
| [set_Color](./set_color/)(System::Drawing::Color) | Setter für [Aspose::Words::Drawing::Fill::get_Color](./get_color/). |
| [set_ForeColor](./set_forecolor/)(System::Drawing::Color) | Setzt ein Color-Objekt, das die Vordergrundfarbe für die Füllung darstellt. |
| [set_ForeThemeColor](./set_forethemecolor/)(Aspose::Words::Themes::ThemeColor) | Setter für [Aspose::Words::Drawing::Fill::get_ForeThemeColor](./get_forethemecolor/). |
| [set_ForeTintAndShade](./set_foretintandshade/)(double) | Setter für [Aspose::Words::Drawing::Fill::get_ForeTintAndShade](./get_foretintandshade/). |
| [set_GradientAngle](./set_gradientangle/)(double) | Setter für [Aspose::Words::Drawing::Fill::get_GradientAngle](./get_gradientangle/). |
| [set_Opacity](./set_opacity/)(double) | Setter für [Aspose::Words::Drawing::Fill::get_Opacity](./get_opacity/). |
| [set_RotateWithObject](./set_rotatewithobject/)(bool) | Legt fest, ob die Füllung mit dem angegebenen Objekt rotiert. |
| [set_TextureAlignment](./set_texturealignment/)(Aspose::Words::Drawing::TextureAlignment) | Setter für [Aspose::Words::Drawing::Fill::get_TextureAlignment](./get_texturealignment/). |
| [set_Transparency](./set_transparency/)(double) | Setter für [Aspose::Words::Drawing::Fill::get_Transparency](./get_transparency/). |
| [set_Visible](./set_visible/)(bool) | Setzt den Wert, der **true** ist, wenn die auf diese Instanz angewendete Formatierung sichtbar ist. |
| [SetImage](./setimage/)(const System::String\&) | Ändert den Fülltyp zu einem einzelnen Bild. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&) | Ändert den Fülltyp zu einem einzelnen Bild. |
| [SetImage](./setimage/)(const System::ArrayPtr\<uint8_t\>\&) | Ändert den Fülltyp zu einem einzelnen Bild. |
| [Solid](./solid/)() | Setzt die Füllung auf eine einheitliche Farbe. |
| [Solid](./solid/)(System::Drawing::Color) | Setzt die Füllung auf eine festgelegte einheitliche Farbe. |
| [TwoColorGradient](./twocolorgradient/)(Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant) | Setzt die angegebene Füllung auf einen Zweifarbverlauf. |
| [TwoColorGradient](./twocolorgradient/)(System::Drawing::Color, System::Drawing::Color, Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant) | Setzt die angegebene Füllung auf einen Zweifarbverlauf. |
| static [Type](./type/)() |  |
## Hinweise


Verwenden Sie die [Fill](../shapebase/get_fill/) oder [Fill](../../aspose.words/font/get_fill/) Eigenschaft, um auf die Füllungseigenschaften eines Objekts zuzugreifen. Sie erstellen keine Instanzen der Klasse [Fill](./) direkt.

## Beispiele



Zeigt, wie man eine Form mit einer einfarbigen Farbe füllt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Schreiben Sie etwas Text und bedecken Sie ihn anschließend mit einer schwebenden Form.
builder->get_Font()->set_Size(32);
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::CloudCallout, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 25, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 25, 250, 150, Aspose::Words::Drawing::WrapType::None);

// Verwenden Sie die Eigenschaft \"StrokeColor\", um die Farbe der Kontur der Form festzulegen.
shape->set_StrokeColor(System::Drawing::Color::get_CadetBlue());

// Verwenden Sie die Eigenschaft \"FillColor\", um die Farbe des Innenbereichs der Form festzulegen.
shape->set_FillColor(System::Drawing::Color::get_LightBlue());

// Die Eigenschaft \"Opacity\" bestimmt, wie transparent die Farbe auf einer Skala von 0 bis 1 ist,
// wobei 1 vollständig undurchsichtig und 0 unsichtbar ist.
// Die Füllung der Form ist standardmäßig vollständig undurchsichtig, sodass wir den Text, über dem sich die Form befindet, nicht sehen können.
ASPOSE_ASSERT_EQ(1.0, shape->get_Fill()->get_Opacity());

// Setzen Sie die Opazität der Füllfarbe der Form auf einen niedrigeren Wert, damit wir den darunter liegenden Text sehen können.
shape->get_Fill()->set_Opacity(0.3);

doc->Save(get_ArtifactsDir() + u"Shape.Fill.docx");
```

## Siehe auch

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
