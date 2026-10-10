---
title: "Aspose::Words::Markup::IStructuredDocumentTag::get_LockContents méthode"
linktitle: "get_LockContents"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Markup::IStructuredDocumentTag::get_LockContents méthode. Lorsqu'elle est définie sur true, cette propriété interdit à l'utilisateur de modifier le contenu de ce SDT en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words.markup/istructureddocumenttag/get_lockcontents/
---
## IStructuredDocumentTag::get_LockContents method


Lorsque la valeur est true, cette propriété empêchera un utilisateur de modifier le contenu de ce **SDT**.

```cpp
virtual bool Aspose::Words::Markup::IStructuredDocumentTag::get_LockContents()=0
```


## Exemples



Montre comment appliquer des restrictions d'édition aux balises de document structuré.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez une balise de document structuré en texte brut, qui agit comme une zone de texte invitant l'utilisateur à la remplir.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// Définissez la propriété \"LockContents\" sur \"true\" pour empêcher l'utilisateur de modifier le contenu de cette zone de texte.
tag->set_LockContents(true);
builder->Write(u"The contents of this structured document tag cannot be edited: ");
builder->InsertNode(tag);

tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// Définissez la propriété \"LockContentControl\" sur \"true\" pour empêcher l'utilisateur de
// supprimer manuellement cette balise de document structuré dans Microsoft Word.
tag->set_LockContentControl(true);

builder->InsertParagraph();
builder->Write(u"This structured document tag cannot be deleted but its contents can be edited: ");
builder->InsertNode(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.Lock.docx");
```

## Voir aussi

* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
