---
title: "Aspose::Words::Drawing::SignatureLine::get_ShowDate méthode"
linktitle: "get_ShowDate"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::SignatureLine::get_ShowDate méthode. Obtient ou définit une valeur indiquant que la date de signature est affichée dans la ligne de signature. La valeur par défaut de cette propriété est true en C++."
type: docs
weight: 10000
url: /fr/cpp/aspose.words.drawing/signatureline/get_showdate/
---
## SignatureLine::get_ShowDate method


Obtient ou définit une valeur indiquant que la date de signature est affichée dans la ligne de signature. La valeur par défaut de cette propriété est **true**.

```cpp
bool Aspose::Words::Drawing::SignatureLine::get_ShowDate()
```


## Exemples



Montre comment créer une ligne de signature et l'insérer dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto options = System::MakeObject<Aspose::Words::SignatureLineOptions>();
options->set_AllowComments(true);
options->set_DefaultInstructions(true);
options->set_Email(u"john.doe@management.com");
options->set_Instructions(u"Please sign here");
options->set_ShowDate(true);
options->set_Signer(u"John Doe");
options->set_SignerTitle(u"Senior Manager");

// Insérez une forme qui contiendra une ligne de signature, dont l'apparence nous allons
// personnaliser en utilisant l'objet "SignatureLineOptions" que nous avons créé ci‑dessus.
// Si nous insérons une forme dont les coordonnées proviennent du coin inférieur droit de la page,
// nous devrons fournir des coordonnées x et y négatives pour faire apparaître la forme.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertSignatureLine(options, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, -170.0, Aspose::Words::Drawing::RelativeVerticalPosition::BottomMargin, -60.0, Aspose::Words::Drawing::WrapType::None);

ASSERT_TRUE(shape->get_IsSignatureLine());

// Vérifiez les propriétés de notre ligne de signature via son objet Shape.
System::SharedPtr<Aspose::Words::Drawing::SignatureLine> signatureLine = shape->get_SignatureLine();

ASSERT_EQ(u"john.doe@management.com", signatureLine->get_Email());
ASSERT_EQ(u"John Doe", signatureLine->get_Signer());
ASSERT_EQ(u"Senior Manager", signatureLine->get_SignerTitle());
ASSERT_EQ(u"Please sign here", signatureLine->get_Instructions());
ASSERT_TRUE(signatureLine->get_ShowDate());
ASSERT_TRUE(signatureLine->get_AllowComments());
ASSERT_TRUE(signatureLine->get_DefaultInstructions());

doc->Save(get_ArtifactsDir() + u"Shape.SignatureLine.docx");
```

## Voir aussi

* Class [SignatureLine](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
