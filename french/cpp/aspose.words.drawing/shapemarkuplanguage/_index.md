---
title: "Aspose::Words::Drawing::ShapeMarkupLanguage énum"
linktitle: "ShapeMarkupLanguage"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ShapeMarkupLanguage énum. Spécifie le langage de balisage utilisé pour la forme en C++."
type: docs
weight: 37000
url: /fr/cpp/aspose.words.drawing/shapemarkuplanguage/
---
## ShapeMarkupLanguage enum


Spécifie le langage [Markup](../../aspose.words.markup/) utilisé pour la forme.

```cpp
enum class ShapeMarkupLanguage : uint8_t
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Dml | 0 | [Drawing](../)[Markup](../../aspose.words.markup/) Le langage est utilisé pour définir la forme. |
| Vml | 1 | Le langage vectoriel [Markup](../../aspose.words.markup/) est utilisé pour définir la forme. |


## Exemples



Montre comment définir une spécification de conformité OOXML pour un document enregistré afin de s'y conformer.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Si nous configurons les options de compatibilité pour être conformes à Microsoft Word 2003,
// l'insertion d'une image définira sa forme en utilisant VML.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2003);
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Vml, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_MarkupLanguage());

// La norme OOXML "ISO/IEC 29500:2008" ne prend pas en charge les formes VML.
// Si nous définissons la propriété "Compliance" de l'objet SaveOptions sur "OoxmlCompliance.Iso29500_2008_Strict",
// tout document que nous enregistrons en passant cet objet devra suivre cette norme.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Docx);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Notre document enregistré définit la forme en utilisant DML pour se conformer à la norme OOXML "ISO/IEC 29500:2008".
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.Iso29500Strict.docx");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Dml, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_MarkupLanguage());
```

## Voir aussi

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
