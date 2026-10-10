---
title: "Méthode Aspose::Words::Saving::TxtSaveOptionsBase::get_ParagraphBreak"
linktitle: "get_ParagraphBreak"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::TxtSaveOptionsBase::get_ParagraphBreak. Spécifie la chaîne à utiliser comme saut de paragraphe lors de l'exportation aux formats texte en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.saving/txtsaveoptionsbase/get_paragraphbreak/
---
## TxtSaveOptionsBase::get_ParagraphBreak method


Spécifie la chaîne à utiliser comme saut de paragraphe lors de l'exportation dans des formats texte.

```cpp
System::String Aspose::Words::Saving::TxtSaveOptionsBase::get_ParagraphBreak() const
```

## Remarques


La valeur par défaut est [CrLf](../../../aspose.words/controlchar/crlf/).

## Exemples



Montre comment enregistrer un document .txt avec un saut de paragraphe personnalisé.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Paragraph 1.");
builder->Writeln(u"Paragraph 2.");
builder->Write(u"Paragraph 3.");

// Créez un objet "TxtSaveOptions" que nous pouvons passer à la méthode "Save" du document
// pour modifier la façon dont nous enregistrons le document en texte brut.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::Text, txtSaveOptions->get_SaveFormat());

// Définissez le "ParagraphBreak" à une valeur personnalisée que nous souhaitons placer à la fin de chaque paragraphe.
txtSaveOptions->set_ParagraphBreak(u" End of paragraph.\n\n\t");

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.ParagraphBreak.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.ParagraphBreak.txt");

ASSERT_EQ(System::String(u"Paragraph 1. End of paragraph.\n\n\t") + u"Paragraph 2. End of paragraph.\n\n\t" + u"Paragraph 3. End of paragraph.\n\n\t", docText);
```

## Voir aussi

* Class [TxtSaveOptionsBase](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
