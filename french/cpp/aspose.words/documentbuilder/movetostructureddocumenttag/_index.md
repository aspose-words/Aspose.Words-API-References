---
title: "Aspose::Words::DocumentBuilder::MoveToStructuredDocumentTag method"
linktitle: "MoveToStructuredDocumentTag"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DocumentBuilder::MoveToStructuredDocumentTag method. Déplace le curseur vers la balise de document structuré en C++."
type: docs
weight: 61000
url: /fr/cpp/aspose.words/documentbuilder/movetostructureddocumenttag/
---
## DocumentBuilder::MoveToStructuredDocumentTag(const System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>\&, int32_t) method


Déplace le curseur vers la balise de document structuré.

```cpp
void Aspose::Words::DocumentBuilder::MoveToStructuredDocumentTag(const System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> &structuredDocumentTag, int32_t characterIndex)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| structuredDocumentTag | const System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>\& | La balise de document structuré vers laquelle se déplacer. |
| characterIndex | int32_t | L'index du caractère à l'intérieur de la balise de document structuré. Une valeur négative vous permet de spécifier une position depuis la fin de la balise de document structuré. Utilisez -1 pour vous déplacer à la fin de la balise de document structuré. Si la balise de document structuré est au niveau du bloc, et que vous souhaitez déplacer le curseur à la fin de son dernier paragraphe, spécifiez -2. |

## Exemples



Montre comment déplacer le curseur de [DocumentBuilder](../) à l'intérieur d'une balise de document structuré.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Il existe plusieurs façons de déplacer le curseur :
// 1 -  Déplacer vers le premier caractère de la balise de document structuré par index.
builder->MoveToStructuredDocumentTag(1, 1);

// 2 -  Déplacer vers le premier caractère de la balise de document structuré par objet.
auto tag = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTag, 2, true));
builder->MoveToStructuredDocumentTag(tag, 1);
builder->Write(u" New text.");

ASSERT_EQ(u"R New text.ichText", tag->GetText().Trim());

// 3 -  Déplacer vers la fin de la deuxième balise de document structuré.
builder->MoveToStructuredDocumentTag(1, -1);
ASSERT_TRUE(builder->get_IsAtEndOfStructuredDocumentTag());

// Obtenir la balise de document structuré actuellement sélectionnée.
builder->get_CurrentStructuredDocumentTag()->set_Color(System::Drawing::Color::get_Green());

doc->Save(get_ArtifactsDir() + u"Document.MoveToStructuredDocumentTag.docx");
```

## Voir aussi

* Class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::MoveToStructuredDocumentTag(int32_t, int32_t) method


Déplace le curseur vers une balise de document structuré dans la section actuelle.

```cpp
void Aspose::Words::DocumentBuilder::MoveToStructuredDocumentTag(int32_t structuredDocumentTagIndex, int32_t characterIndex)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| structuredDocumentTagIndex | int32_t | L'index de la balise de document structuré vers laquelle se déplacer. |
| characterIndex | int32_t | L'index du caractère à l'intérieur de la balise de document structuré. Une valeur négative vous permet de spécifier une position depuis la fin de la balise de document structuré. Utilisez -1 pour vous déplacer à la fin de la balise de document structuré. Si la balise de document structuré est au niveau du bloc, et que vous souhaitez déplacer le curseur à la fin de son dernier paragraphe, spécifiez -2. |
## Remarques


La navigation est effectuée à l'intérieur de l'histoire actuelle de la section actuelle. C’est‑à‑dire, si vous avez déplacé le curseur vers l’en‑tête principal de la première section, alors *structuredDocumentTagIndex* spécifie l'index de la balise de document structuré à l'intérieur de cet en‑tête de cette section.

Lorsque *structuredDocumentTagIndex* est supérieur ou égal à 0, il indique un index à partir du début de la section, 0 étant la première balise de document structuré. Lorsque *structuredDocumentTagIndex* est inférieur à 0, il indique un index à partir de la fin de la section, -1 étant la dernière balise de document structuré.

## Exemples



Montre comment déplacer le curseur de [DocumentBuilder](../) à l'intérieur d'une balise de document structuré.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Il existe plusieurs façons de déplacer le curseur :
// 1 -  Déplacer vers le premier caractère de la balise de document structuré par index.
builder->MoveToStructuredDocumentTag(1, 1);

// 2 -  Déplacer vers le premier caractère de la balise de document structuré par objet.
auto tag = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTag, 2, true));
builder->MoveToStructuredDocumentTag(tag, 1);
builder->Write(u" New text.");

ASSERT_EQ(u"R New text.ichText", tag->GetText().Trim());

// 3 -  Déplacer vers la fin de la deuxième balise de document structuré.
builder->MoveToStructuredDocumentTag(1, -1);
ASSERT_TRUE(builder->get_IsAtEndOfStructuredDocumentTag());

// Obtenir la balise de document structuré actuellement sélectionnée.
builder->get_CurrentStructuredDocumentTag()->set_Color(System::Drawing::Color::get_Green());

doc->Save(get_ArtifactsDir() + u"Document.MoveToStructuredDocumentTag.docx");
```

## Voir aussi

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
