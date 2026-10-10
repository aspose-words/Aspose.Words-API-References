---
title: "Aspose::Words::DocumentBuilder::get_CurrentStructuredDocumentTag method"
linktitle: "get_CurrentStructuredDocumentTag"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DocumentBuilder::get_CurrentStructuredDocumentTag method. Obtient la balise de document structuré actuellement sélectionnée dans ce DocumentBuilder en C++."
type: docs
weight: 15000
url: /fr/cpp/aspose.words/documentbuilder/get_currentstructureddocumenttag/
---
## DocumentBuilder::get_CurrentStructuredDocumentTag method


Obtient la balise de document structuré actuellement sélectionnée dans ce [DocumentBuilder](../).

```cpp
System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> Aspose::Words::DocumentBuilder::get_CurrentStructuredDocumentTag()
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

* Class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
