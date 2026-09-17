---
title: "Méthode Aspose::Words::Paragraph::JoinRunsWithSameFormatting"
linktitle: "JoinRunsWithSameFormatting"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Paragraph::JoinRunsWithSameFormatting. Fusionne les runs ayant le même formatage dans le paragraphe en C++."
type: docs
weight: 31000
url: /fr/cpp/aspose.words/paragraph/joinrunswithsameformatting/
---
## Paragraph::JoinRunsWithSameFormatting() method


Fusionne les segments avec le même formatage dans le paragraphe.

```cpp
int32_t Aspose::Words::Paragraph::JoinRunsWithSameFormatting()
```


### ReturnValue

Nombre de fusions effectuées. Lorsque **N** séquences adjacentes sont fusionnées, elles comptent comme **N - 1** fusions.

## Exemples



Montre comment simplifier les paragraphes en fusionnant les runs superflus.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez quatre runs de texte dans le paragraphe.
builder->Write(u"Run 1. ");
builder->Write(u"Run 2. ");
builder->Write(u"Run 3. ");
builder->Write(u"Run 4. ");

// Si nous ouvrons ce document dans Microsoft Word, le paragraphe apparaîtra comme un corps de texte continu.
// Cependant, il sera composé de quatre runs distincts avec le même formatage. Des paragraphes fragmentés comme celui-ci
// peuvent survenir lorsque nous modifions manuellement plusieurs fois des parties d’un même paragraphe dans Microsoft Word.
System::SharedPtr<Aspose::Words::Paragraph> para = builder->get_CurrentParagraph();

ASSERT_EQ(4, para->get_Runs()->get_Count());

// Modifiez le style du dernier run pour le distinguer des trois premiers.
para->get_Runs()->idx_get(3)->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Emphasis);

// Nous pouvons exécuter la méthode "JoinRunsWithSameFormatting" pour optimiser le contenu du document
// en fusionnant les runs similaires en un seul, réduisant ainsi leur nombre total.
// Cette méthode renvoie également le nombre de runs que cette méthode a fusionnés.
// Ces deux fusions ont eu lieu pour combiner les runs #1, #2 et #3,
// tout en excluant Run #4 parce qu’il a un style incompatible.
ASSERT_EQ(2, para->JoinRunsWithSameFormatting());

// Le nombre de runs restants sera égal au nombre d'origine
// moins le nombre de fusions de runs que la méthode "JoinRunsWithSameFormatting" a effectuées.
ASSERT_EQ(2, para->get_Runs()->get_Count());
ASSERT_EQ(u"Run 1. Run 2. Run 3. ", para->get_Runs()->idx_get(0)->get_Text());
ASSERT_EQ(u"Run 4. ", para->get_Runs()->idx_get(1)->get_Text());
```

## Voir aussi

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::JoinRunsWithSameFormatting(const System::SharedPtr\<Aspose::Words::JoinRunsOptions\>\&) method


Fusionne les segments avec le même formatage dans le paragraphe.

```cpp
int32_t Aspose::Words::Paragraph::JoinRunsWithSameFormatting(const System::SharedPtr<Aspose::Words::JoinRunsOptions> &options)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| options | const System::SharedPtr\<Aspose::Words::JoinRunsOptions\>\& | Options supplémentaires |

### ReturnValue

Nombre de fusions effectuées. Lorsque **N** séquences adjacentes sont fusionnées, elles comptent comme **N - 1** fusions.

## Exemples



Montre comment fusionner des runs avec le même formatage tout en ignorant les attributs redondants et insignifiants.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Créez des runs avec un formatage visible identique mais quelques différences internes.
builder->get_Font()->set_Name(u"Arial");
builder->get_Font()->set_Size(12);
builder->Write(u"Hello ");
builder->Write(u"world");

// Vérifiez les runs avant la fusion.
ASSERT_EQ(2, doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->get_Count());
ASSERT_EQ(u"Hello ", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Text());
ASSERT_EQ(u"world", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(1)->get_Text());

// Configurez les options pour ignorer les attributs redondants et insignifiants lors de la fusion.
auto options = System::MakeObject<Aspose::Words::JoinRunsOptions>();
options->set_IgnoreRedundant(true);
// Ignorez les propriétés de run redondantes qui n'affectent pas l'apparence.
options->set_IgnoreInsignificant(true);
// Ignorez les différences insignifiantes comme les runs composés uniquement d'espaces.

// Fusionnez les segments qui ont le même formatage visible en utilisant les options étendues.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->JoinRunsWithSameFormatting(options);

// Vérifiez que les segments ont été fusionnés avec succès.
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->get_Count());
ASSERT_EQ(u"Hello world", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Text());

doc->Save(get_ArtifactsDir() + u"Paragraph.JoinRunsWithSameFormattingWithOptions.docx");
```

## Voir aussi

* Class [JoinRunsOptions](../../joinrunsoptions/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
