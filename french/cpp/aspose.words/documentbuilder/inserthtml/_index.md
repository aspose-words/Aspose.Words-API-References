---
title: "Aspose::Words::DocumentBuilder::InsertHtml méthode"
linktitle: "InsertHtml"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DocumentBuilder::InsertHtml méthode. Insère une chaîne HTML dans le document en C++."
type: docs
weight: 37000
url: /fr/cpp/aspose.words/documentbuilder/inserthtml/
---
## DocumentBuilder::InsertHtml(const System::String\&) method


Insère une chaîne HTML dans le document.

```cpp
void Aspose::Words::DocumentBuilder::InsertHtml(const System::String &html)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| html | const System::String\& | Une chaîne HTML à insérer dans le document. |

## Exemples



Montre comment utiliser un document builder pour insérer du contenu html dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

const System::String html = System::String(u"<p align='right'>Paragraph right</p>") + u"<b>Implicit paragraph left</b>" + u"<div align='center'>Div center</div>" + u"<h1 align='left'>Heading 1 left.</h1>";

builder->InsertHtml(html);

// L'insertion de code HTML analyse le formatage de chaque élément pour le convertir en formatage de texte équivalent dans le document.
System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(u"Paragraph right", paragraphs->idx_get(0)->GetText().Trim());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());

ASSERT_EQ(u"Implicit paragraph left", paragraphs->idx_get(1)->GetText().Trim());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());
ASSERT_TRUE(paragraphs->idx_get(1)->get_Runs()->idx_get(0)->get_Font()->get_Bold());

ASSERT_EQ(u"Div center", paragraphs->idx_get(2)->GetText().Trim());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Center, paragraphs->idx_get(2)->get_ParagraphFormat()->get_Alignment());

ASSERT_EQ(u"Heading 1 left.", paragraphs->idx_get(3)->GetText().Trim());
ASSERT_EQ(u"Heading 1", paragraphs->idx_get(3)->get_ParagraphFormat()->get_Style()->get_Name());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHtml.docx");
```

## Voir aussi

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertHtml(const System::String\&, Aspose::Words::HtmlInsertOptions) method


Insère une chaîne HTML dans le document. Permet de spécifier des options supplémentaires.

```cpp
void Aspose::Words::DocumentBuilder::InsertHtml(const System::String &html, Aspose::Words::HtmlInsertOptions options)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| html | const System::String\& | Une chaîne HTML à insérer dans le document. |
| options | Aspose::Words::HtmlInsertOptions | Options utilisées lors de l'insertion d'une chaîne HTML. |

## Voir aussi

* Enum [HtmlInsertOptions](../../htmlinsertoptions/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertHtml(const System::String\&, bool) method


Insère une chaîne HTML dans le document.

```cpp
void Aspose::Words::DocumentBuilder::InsertHtml(const System::String &html, bool useBuilderFormatting)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| html | const System::String\& | Une chaîne HTML à insérer dans le document. |
| useBuilderFormatting | bool | Valeur indiquant si le formatage spécifié dans [DocumentBuilder](../) est utilisé comme formatage de base pour le texte importé depuis le HTML. |
## Remarques


Vous pouvez utiliser cette méthode pour insérer un fragment HTML ou un document HTML complet.

Lorsque *useBuilderFormatting* est **false**, le formatage de [DocumentBuilder](../) est ignoré et le formatage du texte inséré est basé sur le formatage HTML par défaut. En conséquence, le texte apparaît tel qu'il est rendu dans les navigateurs.

Lorsque *useBuilderFormatting* est **true**, le formatage du texte inséré est basé sur le formatage de [DocumentBuilder](../), et le texte apparaît comme s'il avait été inséré avec [Write()](../).

## Exemples



Montre comment appliquer le formatage d'un document builder lors de l'insertion de contenu HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Définissez un alignement de texte pour le builder, insérez un paragraphe HTML avec un alignement spécifié, et un autre sans.
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Distributed);
builder->InsertHtml(System::String(u"<p align='right'>Paragraph 1.</p>") + u"<p>Paragraph 2.</p>", useBuilderFormatting);

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

// Le premier paragraphe a un alignement spécifié. Lorsque InsertHtml analyse le code HTML,
// la valeur d'alignement du paragraphe trouvée dans le code HTML l'emporte toujours sur la valeur du document builder.
ASSERT_EQ(u"Paragraph 1.", paragraphs->idx_get(0)->GetText().Trim());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());

// Le deuxième paragraphe n'a aucun alignement spécifié. Il peut voir sa valeur d'alignement remplie
// par la valeur du builder selon le drapeau que nous avons passé à la méthode InsertHtml.
ASSERT_EQ(u"Paragraph 2.", paragraphs->idx_get(1)->GetText().Trim());
ASSERT_EQ(useBuilderFormatting ? Aspose::Words::ParagraphAlignment::Distributed : Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHtmlWithFormatting.docx");
```

## Voir aussi

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
