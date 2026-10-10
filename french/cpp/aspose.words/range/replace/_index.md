---
title: "Aspose::Words::Range::Replace méthode"
linktitle: "Remplacer"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Range::Replace méthode. Remplace toutes les occurrences d'un motif de caractères spécifié par une expression régulière par une autre chaîne en C++."
type: docs
weight: 12000
url: /fr/cpp/aspose.words/range/replace/
---
## Range::Replace(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Remplace toutes les occurrences d'un motif de caractères spécifié par une expression régulière par une autre chaîne.

```cpp
int32_t Aspose::Words::Range::Replace(const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| motif | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Un motif d'expression régulière utilisé pour trouver des correspondances. |
| remplacement | const System::String\& | Une chaîne pour remplacer toutes les occurrences du motif. |

### ReturnValue

Le nombre de remplacements effectués.
## Remarques


Remplace la correspondance entière capturée par l'expression régulière.

La méthode peut traiter les sauts dans les chaînes de motif et de remplacement.

Vous devez utiliser des méta‑caractères spéciaux si vous devez travailler avec des sauts :

* **%&p** - paragraph break
* **%&b** - section break
* **%&m** - page break
* **%&l** - manual line break



## Exemples



Montre comment remplacer toutes les occurrences d'un modèle d'expression régulière par un autre texte.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"I decided to get the curtains in gray, ideal for the grey-accented room.");

doc->get_Range()->Replace(System::MakeObject<System::Text::RegularExpressions::Regex>(u"gr(a|e)y"), u"lavender");

ASSERT_EQ(u"I decided to get the curtains in lavender, ideal for the lavender-accented room.", doc->GetText().Trim());
```

## Voir aussi

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Range::Replace(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Remplace toutes les occurrences d'un motif de caractères spécifié par une expression régulière par une autre chaîne.

```cpp
int32_t Aspose::Words::Range::Replace(const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| motif | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Un motif d'expression régulière utilisé pour trouver des correspondances. |
| remplacement | const System::String\& | Une chaîne pour remplacer toutes les occurrences du motif. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | Objet [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) pour spécifier des options supplémentaires. |

### ReturnValue

Le nombre de remplacements effectués.
## Remarques


Remplace la correspondance entière capturée par l'expression régulière.

La méthode peut traiter les sauts dans les chaînes de motif et de remplacement.

Vous devez utiliser des méta‑caractères spéciaux si vous devez travailler avec des sauts :

* **%&p** - paragraph break
* **%&b** - section break
* **%&m** - page break
* **%&l** - manual line break
* **%&&** - & character



## Voir aussi

* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Range::Replace(const System::String\&, const System::String\&) method


Remplace toutes les occurrences d'un motif de chaîne de caractères spécifié par une chaîne de remplacement.

```cpp
int32_t Aspose::Words::Range::Replace(const System::String &pattern, const System::String &replacement)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| motif | const System::String\& | Une chaîne à remplacer. |
| remplacement | const System::String\& | Une chaîne pour remplacer toutes les occurrences du motif. |

### ReturnValue

Le nombre de remplacements effectués.
## Remarques


Le modèle ne sera pas utilisé comme expression régulière. Veuillez utiliser [Replace()](../) si vous avez besoin d'expressions régulières.

Utilise une comparaison insensible à la casse.

La méthode peut traiter les sauts dans les chaînes de motif et de remplacement.

Vous devez utiliser des méta‑caractères spéciaux si vous devez travailler avec des sauts :

* **%&p** - paragraph break
* **%&b** - section break
* **%&m** - page break
* **%&l** - manual line break



## Exemples



Montre comment effectuer une opération de recherche et remplacement de texte sur le contenu d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Greetings, _FullName_!");

// Effectuez une opération de recherche et remplacement sur le contenu de notre document et vérifiez le nombre de remplacements effectués.
int32_t replacementCount = doc->get_Range()->Replace(u"_FullName_", u"John Doe");

ASSERT_EQ(1, replacementCount);
ASSERT_EQ(u"Greetings, John Doe!", doc->GetText().Trim());
```


Montre comment ajouter du formatage aux paragraphes dans lesquels une opération de recherche et remplacement a trouvé des correspondances.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Every paragraph that ends with a full stop like this one will be right aligned.");
builder->Writeln(u"This one will not!");
builder->Write(u"This one also will.");

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(2)->get_ParagraphFormat()->get_Alignment());

// Nous pouvons utiliser un objet "FindReplaceOptions" pour modifier le processus de recherche et remplacement.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Définissez la propriété "Alignment" sur "ParagraphAlignment.Right" pour aligner à droite chaque paragraphe.
// qui contient une correspondance trouvée par l'opération de recherche et remplacement.
options->get_ApplyParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Right);

// Remplacez chaque point final qui se trouve juste avant un saut de paragraphe par un point d'exclamation.
int32_t count = doc->get_Range()->Replace(u".&p", u"!&p", options);

ASSERT_EQ(2, count);
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(2)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(System::String(u"Every paragraph that ends with a full stop like this one will be right aligned!\r") + u"This one will not!\r" + u"This one also will!", doc->GetText().Trim());
```

## Voir aussi

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Range::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Remplace toutes les occurrences d'un motif de chaîne de caractères spécifié par une chaîne de remplacement.

```cpp
int32_t Aspose::Words::Range::Replace(const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| motif | const System::String\& | Une chaîne à remplacer. |
| remplacement | const System::String\& | Une chaîne pour remplacer toutes les occurrences du motif. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | Objet [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) pour spécifier des options supplémentaires. |

### ReturnValue

Le nombre de remplacements effectués.
## Remarques


Le modèle ne sera pas utilisé comme expression régulière. Veuillez utiliser [Replace()](../) si vous avez besoin d'expressions régulières.

La méthode peut traiter les sauts dans les chaînes de motif et de remplacement.

Vous devez utiliser des méta‑caractères spéciaux si vous devez travailler avec des sauts :

* **%&p** - paragraph break
* **%&b** - section break
* **%&m** - page break
* **%&l** - manual line break
* **%&&** - & character



## Exemples



Montre comment remplacer du texte dans le pied de page d’un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footer.docx");

System::SharedPtr<Aspose::Words::HeaderFooterCollection> headersFooters = doc->get_FirstSection()->get_HeadersFooters();
System::SharedPtr<Aspose::Words::HeaderFooter> footer = headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_MatchCase(false);
options->set_FindWholeWordsOnly(false);

int32_t currentYear = System::DateTime::get_Now().get_Year();
footer->get_Range()->Replace(u"(C) 2006 Aspose Pty Ltd.", System::String::Format(u"Copyright (C) {0} by Aspose Pty Ltd.", currentYear), options);

doc->Save(get_ArtifactsDir() + u"HeaderFooter.ReplaceText.docx");
```


Montre comment activer/désactiver la sensibilité à la casse lors d'une opération de recherche et remplacement.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Ruby bought a ruby necklace.");

// Nous pouvons utiliser un objet "FindReplaceOptions" pour modifier le processus de recherche et remplacement.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Définissez le drapeau "MatchCase" sur "true" pour appliquer la sensibilité à la casse lors de la recherche des chaînes à remplacer.
// Définissez le drapeau "MatchCase" sur "false" pour ignorer la casse des caractères lors de la recherche du texte à remplacer.
options->set_MatchCase(matchCase);

doc->get_Range()->Replace(u"Ruby", u"Jade", options);

ASSERT_EQ(matchCase ? System::String(u"Jade bought a ruby necklace.") : System::String(u"Jade bought a Jade necklace."), doc->GetText().Trim());
```


Montre comment activer/désactiver les opérations de recherche et remplacement limitées aux mots isolés.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Jackson will meet you in Jacksonville.");

// Nous pouvons utiliser un objet "FindReplaceOptions" pour modifier le processus de recherche et remplacement.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Définissez le drapeau "FindWholeWordsOnly" sur "true" pour remplacer le texte trouvé s'il ne fait pas partie d'un autre mot.
// Définissez le drapeau "FindWholeWordsOnly" sur "false" pour remplacer tout le texte, quel que soit son contexte.
options->set_FindWholeWordsOnly(findWholeWordsOnly);

doc->get_Range()->Replace(u"Jackson", u"Louis", options);

ASSERT_EQ(findWholeWordsOnly ? System::String(u"Louis will meet you in Jacksonville.") : System::String(u"Louis will meet you in Louisville."), doc->GetText().Trim());
```


Montre comment remplacer toutes les instances de chaîne de texte dans un tableau et une cellule.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Carrots");
builder->InsertCell();
builder->Write(u"50");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Potatoes");
builder->InsertCell();
builder->Write(u"50");
builder->EndTable();

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_MatchCase(true);
options->set_FindWholeWordsOnly(true);

// Effectuez une opération de recherche et remplacement sur un tableau entier.
table->get_Range()->Replace(u"Carrots", u"Eggs", options);

// Effectuez une opération de recherche et remplacement sur la dernière cellule de la dernière ligne du tableau.
table->get_LastRow()->get_LastCell()->get_Range()->Replace(u"50", u"20", options);

ASSERT_EQ(System::String(u"Eggs\a50\a\a") + u"Potatoes\a20\a\a", table->GetText().Trim());
```

## Voir aussi

* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
