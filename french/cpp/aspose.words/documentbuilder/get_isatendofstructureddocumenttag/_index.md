---
title: "Aspose::Words::DocumentBuilder::get_IsAtEndOfStructuredDocumentTag method"
linktitle: "get_IsAtEndOfStructuredDocumentTag"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DocumentBuilder::get_IsAtEndOfStructuredDocumentTag method. Retourne true si le curseur se trouve à la fin d'une balise de document structuré en C++."
type: docs
weight: 19000
url: /fr/cpp/aspose.words/documentbuilder/get_isatendofstructureddocumenttag/
---
## DocumentBuilder::get_IsAtEndOfStructuredDocumentTag method


Renvoie **true** si le curseur est à la fin d'une balise de document structuré.

```cpp
bool Aspose::Words::DocumentBuilder::get_IsAtEndOfStructuredDocumentTag()
```


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
