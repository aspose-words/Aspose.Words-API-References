---
title: "Aspose::Words::DocumentBuilder::PushFont méthode"
linktitle: "PushFont"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DocumentBuilder::PushFont méthode. Enregistre le formatage de caractères actuel sur la pile en C++."
type: docs
weight: 63000
url: /fr/cpp/aspose.words/documentbuilder/pushfont/
---
## DocumentBuilder::PushFont method


Enregistre le formatage de caractères actuel sur la pile.

```cpp
void Aspose::Words::DocumentBuilder::PushFont()
```


## Exemples



Montre comment utiliser la pile de formatage d'un document builder.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Configure le formatage de la police, puis écris le texte qui précède le lien hypertexte.
builder->get_Font()->set_Name(u"Arial");
builder->get_Font()->set_Size(24);
builder->Write(u"To visit Google, hold Ctrl and click ");

// Préserve notre configuration de formatage actuelle sur la pile.
builder->PushFont();

// Modifie le formatage actuel du builder en appliquant un nouveau style.
builder->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Hyperlink);
builder->InsertHyperlink(u"here", u"http://www.google.com", false);

ASSERT_EQ(System::Drawing::Color::get_Blue().ToArgb(), builder->get_Font()->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Underline::Single, builder->get_Font()->get_Underline());

// Restaure le formatage de la police que nous avons enregistré précédemment et supprime l'élément de la pile.
builder->PopFont();

ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), builder->get_Font()->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Underline::None, builder->get_Font()->get_Underline());

builder->Write(u". We hope you enjoyed the example.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.PushPopFont.docx");
```

## Voir aussi

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
