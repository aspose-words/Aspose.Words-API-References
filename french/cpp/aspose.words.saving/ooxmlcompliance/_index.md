---
title: "Aspose::Words::Saving::OoxmlCompliance enum"
linktitle: "OoxmlCompliance"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::OoxmlCompliance enum. Permet de spécifier quelle spécification OOXML sera utilisée lors de l'enregistrement au format DOCX en C++."
type: docs
weight: 72000
url: /fr/cpp/aspose.words.saving/ooxmlcompliance/
---
## OoxmlCompliance enum


Permet de spécifier quelle spécification OOXML sera utilisée lors de l’enregistrement au format DOCX.

```cpp
enum class OoxmlCompliance
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Ecma376_2006 | 0 | ECMA-376 1re édition, 2006. |
| Iso29500_2008_Transitional | 1 | Niveau de conformité Transitional ISO/IEC 29500:2008. |
| Iso29500_2008_Strict | 2 | Niveau de conformité Strict ISO/IEC 29500:2008. |


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


Montre comment configurer une liste pour redémarrer la numérotation à chaque section.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->idx_get(0);
list->set_IsRestartAtEachSection(restartListAtEachSection);

// La propriété "IsRestartAtEachSection" ne sera applicable que lorsque
// le niveau de conformité OOXML du document correspond à une norme plus récente que "OoxmlComplianceCore.Ecma376".
auto options = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
options->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);

builder->get_ListFormat()->set_List(list);

builder->Writeln(u"List item 1");
builder->Writeln(u"List item 2");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Writeln(u"List item 3");
builder->Writeln(u"List item 4");

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.RestartingDocumentList.docx", options);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.RestartingDocumentList.docx");

ASPOSE_ASSERT_EQ(restartListAtEachSection, doc->get_Lists()->idx_get(0)->get_IsRestartAtEachSection());
```


Montre comment insérer des formes DML dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Voici deux types d'habillage que les formes peuvent avoir.
// 1 -  Flottant :
builder->InsertShape(Aspose::Words::Drawing::ShapeType::TopCornersRounded, Aspose::Words::Drawing::RelativeHorizontalPosition::Page, 100, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 100, 50, 50, Aspose::Words::Drawing::WrapType::None);

// 2 -  En ligne :
builder->InsertShape(Aspose::Words::Drawing::ShapeType::DiagonalCornersRounded, 50, 50);

// Si vous devez créer des formes "non-primitive", telles que SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, ou DiagonalCornersRounded,
// alors enregistrez le document avec la conformité "Strict" ou "Transitional", ce qui permet d'enregistrer la forme en tant que DML.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);

doc->Save(get_ArtifactsDir() + u"Shape.ShapeInsertion.docx", saveOptions);
```

## Voir aussi

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
