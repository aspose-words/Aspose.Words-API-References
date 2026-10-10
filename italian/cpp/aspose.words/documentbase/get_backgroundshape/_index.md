---
title: "Metodo Aspose::Words::DocumentBase::get_BackgroundShape"
linktitle: "get_BackgroundShape"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::DocumentBase::get_BackgroundShape. Ottiene o imposta la forma di sfondo del documento. Può essere null in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words/documentbase/get_backgroundshape/
---
## DocumentBase::get_BackgroundShape method


Ottiene o imposta la forma di sfondo del documento. Può essere **null**.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBase::get_BackgroundShape() const
```

## Note


Microsoft Word consente solo una forma la cui proprietà [ShapeType](../../../aspose.words.drawing/shapebase/get_shapetype/) è uguale a [Rectangle](../../../aspose.words.drawing/shapetype/) da utilizzare come forma di sfondo per un documento.

Microsoft Word supporta solo le proprietà di riempimento di una forma di sfondo. Tutte le altre proprietà vengono ignorate.

Impostare questa proprietà a un valore non null imposterà anche [DisplayBackgroundShape](../../../aspose.words.settings/viewoptions/get_displaybackgroundshape/) a **true**.

## Esempi



Mostra come impostare una forma di sfondo per ogni pagina di un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_TRUE(System::TestTools::IsNull(doc->get_BackgroundShape()));

// L'unico tipo di forma che possiamo usare come sfondo è un rettangolo.
auto shapeRectangle = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);

// Ci sono due modi per utilizzare questa forma come sfondo di pagina.
// 1 -  Un colore uniforme:
shapeRectangle->set_FillColor(System::Drawing::Color::get_LightBlue());
doc->set_BackgroundShape(shapeRectangle);

doc->Save(get_ArtifactsDir() + u"DocumentBase.BackgroundShape.FlatColor.docx");

// 2 -  Un'immagine:
shapeRectangle = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shapeRectangle->get_ImageData()->SetImage(get_ImageDir() + u"Transparent background logo.png");

// Regola l'aspetto dell'immagine per renderla più adatta come filigrana.
shapeRectangle->get_ImageData()->set_Contrast(0.2);
shapeRectangle->get_ImageData()->set_Brightness(0.7);

doc->set_BackgroundShape(shapeRectangle);

ASSERT_TRUE(doc->get_BackgroundShape()->get_HasImage());

auto saveOptions = System::MakeObject<Aspose::Words::Saving::PdfSaveOptions>();
saveOptions->set_CacheBackgroundGraphics(false);

// Microsoft Word non supporta forme con immagini come sfondi,
// ma possiamo comunque vedere questi sfondi in altri formati di salvataggio come .pdf.
doc->Save(get_ArtifactsDir() + u"DocumentBase.BackgroundShape.Image.pdf", saveOptions);
```

## Vedi anche

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
