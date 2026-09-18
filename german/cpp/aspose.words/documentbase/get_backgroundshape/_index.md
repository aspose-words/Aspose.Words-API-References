---
title: "Aspose::Words::DocumentBase::get_BackgroundShape Methode"
linktitle: "get_BackgroundShape"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBase::get_BackgroundShape Methode. Gibt die Hintergrundform des Dokuments zurück oder setzt sie. Kann in C++ null sein."
type: docs
weight: 2000
url: /de/cpp/aspose.words/documentbase/get_backgroundshape/
---
## DocumentBase::get_BackgroundShape method


Liest oder legt die Hintergrundform des Dokuments fest. Kann **null** sein.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBase::get_BackgroundShape() const
```

## Hinweise


Microsoft Word erlaubt nur eine Form, deren [ShapeType](../../../aspose.words.drawing/shapebase/get_shapetype/) Eigenschaft gleich [Rectangle](../../../aspose.words.drawing/shapetype/) ist, um als Hintergrundform für ein Dokument verwendet zu werden.

Microsoft Word unterstützt nur die Füll‑Eigenschaften einer Hintergrundform. Alle anderen Eigenschaften werden ignoriert.

Das Setzen dieser Eigenschaft auf einen Nicht‑Null‑Wert wird außerdem das [DisplayBackgroundShape](../../../aspose.words.settings/viewoptions/get_displaybackgroundshape/) auf **true** setzen.

## Beispiele



Zeigt, wie man für jede Seite eines Dokuments eine Hintergrundform festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_TRUE(System::TestTools::IsNull(doc->get_BackgroundShape()));

// Der einzige Formtyp, den wir als Hintergrund verwenden können, ist ein Rechteck.
auto shapeRectangle = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);

// Es gibt zwei Möglichkeiten, diese Form als Seitenhintergrund zu verwenden.
// 1 -  Eine einfarbige Farbe:
shapeRectangle->set_FillColor(System::Drawing::Color::get_LightBlue());
doc->set_BackgroundShape(shapeRectangle);

doc->Save(get_ArtifactsDir() + u"DocumentBase.BackgroundShape.FlatColor.docx");

// 2 -  Ein Bild:
shapeRectangle = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shapeRectangle->get_ImageData()->SetImage(get_ImageDir() + u"Transparent background logo.png");

// Passen Sie das Aussehen des Bildes an, um es besser als Wasserzeichen zu nutzen.
shapeRectangle->get_ImageData()->set_Contrast(0.2);
shapeRectangle->get_ImageData()->set_Brightness(0.7);

doc->set_BackgroundShape(shapeRectangle);

ASSERT_TRUE(doc->get_BackgroundShape()->get_HasImage());

auto saveOptions = System::MakeObject<Aspose::Words::Saving::PdfSaveOptions>();
saveOptions->set_CacheBackgroundGraphics(false);

// Microsoft Word unterstützt keine Formen mit Bildern als Hintergründen,
// aber wir können diese Hintergründe dennoch in anderen Speicherformaten wie .pdf sehen.
doc->Save(get_ArtifactsDir() + u"DocumentBase.BackgroundShape.Image.pdf", saveOptions);
```

## Siehe auch

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
