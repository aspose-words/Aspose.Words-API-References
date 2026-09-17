---
title: "Aspose::Words::DocumentBuilder::MoveToParagraph method"
linktitle: "MoveToParagraph"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DocumentBuilder::MoveToParagraph method. Déplace le curseur vers un paragraphe dans la section actuelle en C++."
type: docs
weight: 59000
url: /fr/cpp/aspose.words/documentbuilder/movetoparagraph/
---
## DocumentBuilder::MoveToParagraph method


Déplace le curseur vers un paragraphe dans la section actuelle.

```cpp
void Aspose::Words::DocumentBuilder::MoveToParagraph(int32_t paragraphIndex, int32_t characterIndex)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| paragraphIndex | int32_t | L'index du paragraphe vers lequel se déplacer. |
| characterIndex | int32_t | L'index du caractère à l'intérieur du paragraphe. Une valeur négative vous permet de spécifier une position depuis la fin du paragraphe. Utilisez -1 pour vous déplacer à la fin du paragraphe. |
## Remarques


La navigation est effectuée à l'intérieur de l'histoire actuelle de la section actuelle. C'est-à-dire, si vous avez déplacé le curseur vers l'en-tête principal de la première section, alors *paragraphIndex* spécifie l'index du paragraphe à l'intérieur de cet en-tête de cette section.

Lorsque *paragraphIndex* est supérieur ou égal à 0, il spécifie un index depuis le début de la section, 0 étant le premier paragraphe. Lorsque *paragraphIndex* est inférieur à 0, il spécifie un index depuis la fin de la section, -1 étant le dernier paragraphe.

## Exemples



Montre comment déplacer la position du curseur d'un constructeur vers un paragraphe spécifié.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");
System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(22, paragraphs->get_Count());

// Créez un constructeur de document pour modifier le document. Le curseur du constructeur,
// qui est le point où il insérera de nouveaux nœuds lorsque nous appelons ses méthodes de construction de document,
// se trouve actuellement au début du document.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

ASSERT_EQ(0, paragraphs->IndexOf(builder->get_CurrentParagraph()));

// Déplacer ce curseur vers un paragraphe différent placera ce curseur devant ce paragraphe.
builder->MoveToParagraph(2, 0);

// Tout nouveau contenu que nous ajoutons sera inséré à ce point.
builder->Writeln(u"This is a new third paragraph. ");
```

## Voir aussi

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
