---
title: "Aspose::Words::Document::UpdateFields méthode"
linktitle: "UpdateFields"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::UpdateFields méthode. Met à jour les valeurs des champs dans l'ensemble du document en C++."
type: docs
weight: 96000
url: /fr/cpp/aspose.words/document/updatefields/
---
## Document::UpdateFields method


Met à jour les valeurs des champs dans l'ensemble du document.

```cpp
void Aspose::Words::Document::UpdateFields()
```

## Remarques


Lorsque vous ouvrez, modifiez puis enregistrez un document, Aspose.Words ne met pas à jour les champs automatiquement, il les conserve intacts. Par conséquent, vous souhaiterez généralement appeler cette méthode avant d'enregistrer si vous avez modifié le document de manière programmatique et souhaitez vous assurer que les valeurs de champ appropriées (calculées) apparaissent dans le document enregistré.

Il n'est pas nécessaire de mettre à jour les champs après l'exécution d'une fusion de courrier car la fusion de courrier est une forme de mise à jour des champs et met automatiquement à jour tous les champs du document.

Cette méthode ne met pas à jour tous les types de champs. Pour la liste détaillée des types de champs pris en charge, consultez le Guide du programmeur.

Cette méthode ne met pas à jour les champs liés aux algorithmes de mise en page (par ex. PAGE, PAGES, PAGEREF). Les champs liés à la mise en page sont mis à jour lorsque vous rendez un document ou appelez [UpdatePageLayout](../updatepagelayout/).

Utilisez la méthode [NormalizeFieldTypes](../normalizefieldtypes/) avant la mise à jour des champs s'il y a eu des modifications du document qui ont affecté les types de champs.

Pour mettre à jour les champs dans une partie spécifique du document, utilisez [UpdateFields](../../range/updatefields/).

## Exemples



Montre comment insérer une Table des matières (TOC) dans un document en utilisant les styles de titres comme entrées.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez une table des matières pour la première page du document.
// Configurez la table pour récupérer les paragraphes avec des titres de niveaux 1 à 3.
// De plus, définissez ses entrées comme des hyperliens qui nous mèneront
// à l’emplacement du titre lorsqu’on clique dessus avec le bouton gauche dans Microsoft Word.
builder->InsertTableOfContents(u"\\o \"1-3\" \\h \\z \\u");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Remplissez la table des matières en ajoutant des paragraphes avec des styles de titres.
// Chaque titre de ce type avec un niveau compris entre 1 et 3 créera une entrée dans la table.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 2");
builder->Writeln(u"Heading 3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading3);
builder->Writeln(u"Heading 3.1.1");
builder->Writeln(u"Heading 3.1.2");
builder->Writeln(u"Heading 3.1.3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading4);
builder->Writeln(u"Heading 3.1.3.1");
builder->Writeln(u"Heading 3.1.3.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.2");
builder->Writeln(u"Heading 3.3");

// Une table des matières est un champ d'un type qui doit être mis à jour pour afficher un résultat à jour.
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertToc.docx");
```


Montre comment utiliser le champ QUOTE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez un champ QUOTE, qui affichera la valeur de sa propriété Text.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldQuote>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldQuote, true));
field->set_Text(u"\"Quoted text\"");

ASSERT_EQ(u" QUOTE  \"\\\"Quoted text\\\"\"", field->GetFieldCode());

// Insérez un champ QUOTE et imbriquez-y un champ DATE.
// Les champs DATE mettent à jour leur valeur à la date actuelle chaque fois que nous ouvrons le document avec Microsoft Word.
// Imbriquer le champ DATE à l'intérieur du champ QUOTE de cette manière figera sa valeur
// à la date à laquelle nous avons créé le document.
builder->Write(u"\nDocument creation date: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldQuote>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldQuote, true));
builder->MoveTo(field->get_Separator());
builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true);

ASSERT_EQ(System::String(u" QUOTE \u0013 DATE \u0014") + System::DateTime::get_Now().get_Date().ToShortDateString() + u"\u0015", field->GetFieldCode());

// Mettez à jour tous les champs pour afficher leurs résultats corrects.
doc->UpdateFields();

ASSERT_EQ(u"\"Quoted text\"", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.QUOTE.docx");
```


Montre comment définir les détails de l'utilisateur et les afficher à l'aide de champs.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Créez un objet UserInformation et définissez-le comme source de données pour les champs qui affichent les informations de l'utilisateur.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Name(u"John Doe");
userInformation->set_Initials(u"J. D.");
userInformation->set_Address(u"123 Main Street");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// Insérez les champs USERNAME, USERINITIALS et USERADDRESS, qui affichent les valeurs de
// les propriétés respectives de l'objet UserInformation que nous avons créé ci-dessus.
ASSERT_EQ(userInformation->get_Name(), builder->InsertField(u" USERNAME ")->get_Result());
ASSERT_EQ(userInformation->get_Initials(), builder->InsertField(u" USERINITIALS ")->get_Result());
ASSERT_EQ(userInformation->get_Address(), builder->InsertField(u" USERADDRESS ")->get_Result());

// L'objet d'options de champ possède également un utilisateur par défaut statique auquel les champs de tous les documents peuvent se référer.
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Name(u"Default User");
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Initials(u"D. U.");
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Address(u"One Microsoft Way");
doc->get_FieldOptions()->set_CurrentUser(Aspose::Words::Fields::UserInformation::get_DefaultUser());

ASSERT_EQ(u"Default User", builder->InsertField(u" USERNAME ")->get_Result());
ASSERT_EQ(u"D. U.", builder->InsertField(u" USERINITIALS ")->get_Result());
ASSERT_EQ(u"One Microsoft Way", builder->InsertField(u" USERADDRESS ")->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"FieldOptions.CurrentUser.docx");
```

## Voir aussi

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
