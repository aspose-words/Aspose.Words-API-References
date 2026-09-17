---
title: "Méthode Aspose::Words::ControlChar::Cr"
linktitle: "Cr"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::ControlChar::Cr. Caractère de retour chariot : \"\\x000d\" ou \"\\r\". Identique à ParagraphBreak en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words/controlchar/cr/
---
## ControlChar::Cr method


Caractère de retour chariot : "\x000d" ou "\r". Identique à [ParagraphBreak](../paragraphbreak/).

```cpp
static System::String & Aspose::Words::ControlChar::Cr()
```


## Exemples



Montre comment utiliser les caractères de contrôle.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérer des paragraphes avec du texte à l'aide de DocumentBuilder.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

// La conversion du document en texte révèle que les caractères de contrôle
// représentent certains des éléments structurels du document, tels que les sauts de page.
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + System::String::Format(u"Hello again!{0}", Aspose::Words::ControlChar::Cr()) + Aspose::Words::ControlChar::PageBreak(), doc->GetText());

// Lors de la conversion d'un document en chaîne de caractères,
// nous pouvons omettre certains caractères de contrôle avec la méthode Trim.
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + u"Hello again!", doc->GetText().Trim());
```

## Voir aussi

* Class [ControlChar](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
