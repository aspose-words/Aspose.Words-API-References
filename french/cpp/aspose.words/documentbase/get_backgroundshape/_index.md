---
title: "Méthode Aspose::Words::DocumentBase::get_BackgroundShape"
linktitle: "get_BackgroundShape"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::DocumentBase::get_BackgroundShape. Obtient ou définit la forme d'arrière-plan du document. Peut être nul en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words/documentbase/get_backgroundshape/
---
## DocumentBase::get_BackgroundShape method


Obtient ou définit la forme d'arrière-plan du document. Peut être **null**.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBase::get_BackgroundShape() const
```

## Remarques


Microsoft Word autorise uniquement une forme dont la propriété [ShapeType](../../../aspose.words.drawing/shapebase/get_shapetype/) est égale à [Rectangle](../../../aspose.words.drawing/shapetype/) pour être utilisée comme forme d'arrière-plan d'un document.

Microsoft Word ne prend en charge que les propriétés de remplissage d'une forme d'arrière-plan. Toutes les autres propriétés sont ignorées.

Définir cette propriété à une valeur non nulle définira également [DisplayBackgroundShape](../../../aspose.words.settings/viewoptions/get_displaybackgroundshape/) sur **true**.

## Exemples



Montre comment définir une forme d'arrière-plan pour chaque page d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_TRUE(System::TestTools::IsNull(doc->get_BackgroundShape()));

// Le seul type de forme que nous pouvons utiliser comme arrière-plan est un rectangle.
auto shapeRectangle = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);

// Il existe deux façons d'utiliser cette forme comme arrière-plan de page.
// 1 -  Une couleur unie :
shapeRectangle->set_FillColor(System::Drawing::Color::get_LightBlue());
doc->set_BackgroundShape(shapeRectangle);

doc->Save(get_ArtifactsDir() + u"DocumentBase.BackgroundShape.FlatColor.docx");

// 2 -  Une image :
shapeRectangle = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shapeRectangle->get_ImageData()->SetImage(get_ImageDir() + u"Transparent background logo.png");

// Ajustez l'apparence de l'image pour la rendre plus adaptée comme filigrane.
shapeRectangle->get_ImageData()->set_Contrast(0.2);
shapeRectangle->get_ImageData()->set_Brightness(0.7);

doc->set_BackgroundShape(shapeRectangle);

ASSERT_TRUE(doc->get_BackgroundShape()->get_HasImage());

auto saveOptions = System::MakeObject<Aspose::Words::Saving::PdfSaveOptions>();
saveOptions->set_CacheBackgroundGraphics(false);

// Microsoft Word ne prend pas en charge les formes avec des images comme arrière-plan,
// mais nous pouvons toujours voir ces arrière-plans dans d'autres formats d'enregistrement tels que .pdf.
doc->Save(get_ArtifactsDir() + u"DocumentBase.BackgroundShape.Image.pdf", saveOptions);
```

## Voir aussi

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
