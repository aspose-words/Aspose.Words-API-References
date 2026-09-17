---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_IsTemporary méthode"
linktitle: "get_IsTemporary"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_IsTemporary méthode. Spécifie si ce SDT doit être supprimé du document WordProcessingML lorsque son contenu est modifié en C++."
type: docs
weight: 19000
url: /fr/cpp/aspose.words.markup/structureddocumenttag/get_istemporary/
---
## StructuredDocumentTag::get_IsTemporary method


Spécifie si ce **SDT** doit être supprimé du document WordProcessingML lorsque son contenu est modifié.

```cpp
bool Aspose::Words::Markup::StructuredDocumentTag::get_IsTemporary() const
```


## Exemples



Montre comment créer des contrôles à usage unique.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Insérez une balise de document structuré en texte brut,
// qui agira comme un formulaire en texte brut dans lequel l'utilisateur peut saisir du texte.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// Définissez la propriété "IsTemporary" sur "true" pour faire disparaître la balise de document structuré et
// assimiler son contenu dans le document après que l'utilisateur l'ait modifié une fois dans Microsoft Word.
// Définissez la propriété "IsTemporary" sur "false" pour permettre à l'utilisateur de modifier le contenu
// de la balise de document structuré un nombre illimité de fois.
tag->set_IsTemporary(isTemporary);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Please enter text: ");
builder->InsertNode(tag);

// Insérez une autre balise de document structuré sous forme de case à cocher et définissez son état par défaut sur "checked".
tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Checkbox, Aspose::Words::Markup::MarkupLevel::Inline);
tag->set_Checked(true);

// Définissez la propriété "IsTemporary" sur "true" pour que la case à cocher devienne un symbole
// une fois que l'utilisateur clique dessus dans Microsoft Word.
// Définissez la propriété "IsTemporary" sur "false" pour permettre à l'utilisateur de cliquer sur la case à cocher un nombre illimité de fois.
tag->set_IsTemporary(isTemporary);

builder->Write(u"\nPlease click the check box: ");
builder->InsertNode(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.IsTemporary.docx");
```

## Voir aussi

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
