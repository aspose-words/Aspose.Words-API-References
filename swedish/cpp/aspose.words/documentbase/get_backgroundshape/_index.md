---
title: "Aspose::Words::DocumentBase::get_BackgroundShape metod"
linktitle: "get_BackgroundShape"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBase::get_BackgroundShape metod. Hämtar eller anger bakgrundsformen för dokumentet. Kan vara null i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words/documentbase/get_backgroundshape/
---
## DocumentBase::get_BackgroundShape method


Hämtar eller anger bakgrundsformen för dokumentet. Kan vara **null**.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBase::get_BackgroundShape() const
```

## Anmärkningar


Microsoft Word tillåter endast en form som har sin egenskap [ShapeType](../../../aspose.words.drawing/shapebase/get_shapetype/) lika med [Rectangle](../../../aspose.words.drawing/shapetype/) för att användas som bakgrundsform för ett dokument.

Microsoft Word stöder endast fyllningsegenskaperna för en bakgrundsform. Alla andra egenskaper ignoreras.

Att sätta denna egenskap till ett icke‑null‑värde kommer också att sätta [DisplayBackgroundShape](../../../aspose.words.settings/viewoptions/get_displaybackgroundshape/) till **true**.

## Exempel



Visar hur man ställer in en bakgrundsform för varje sida i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_TRUE(System::TestTools::IsNull(doc->get_BackgroundShape()));

// Den enda formtypen som vi kan använda som bakgrund är en rektangel.
auto shapeRectangle = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);

// Det finns två sätt att använda denna form som sidbakgrund.
// 1 -  En enfärgad färg:
shapeRectangle->set_FillColor(System::Drawing::Color::get_LightBlue());
doc->set_BackgroundShape(shapeRectangle);

doc->Save(get_ArtifactsDir() + u"DocumentBase.BackgroundShape.FlatColor.docx");

// 2 -  En bild:
shapeRectangle = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shapeRectangle->get_ImageData()->SetImage(get_ImageDir() + u"Transparent background logo.png");

// Justera bildens utseende för att göra den mer lämplig som vattenstämpel.
shapeRectangle->get_ImageData()->set_Contrast(0.2);
shapeRectangle->get_ImageData()->set_Brightness(0.7);

doc->set_BackgroundShape(shapeRectangle);

ASSERT_TRUE(doc->get_BackgroundShape()->get_HasImage());

auto saveOptions = System::MakeObject<Aspose::Words::Saving::PdfSaveOptions>();
saveOptions->set_CacheBackgroundGraphics(false);

// Microsoft Word stöder inte former med bilder som bakgrunder,
// men vi kan fortfarande se dessa bakgrunder i andra sparformat som .pdf.
doc->Save(get_ArtifactsDir() + u"DocumentBase.BackgroundShape.Image.pdf", saveOptions);
```

## Se även

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
