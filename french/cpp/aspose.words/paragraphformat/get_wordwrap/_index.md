---
title: "Méthode Aspose::Words::ParagraphFormat::get_WordWrap"
linktitle: "get_WordWrap"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::ParagraphFormat::get_WordWrap. Si cette propriété est false, le texte latin au milieu d'un mot peut être renvoyé à la ligne pour le paragraphe actuel. Sinon, le texte latin est renvoyé à la ligne par mots entiers en C++."
type: docs
weight: 42000
url: /fr/cpp/aspose.words/paragraphformat/get_wordwrap/
---
## ParagraphFormat::get_WordWrap method


Si cette propriété est **false**, le texte latin au milieu d’un mot peut être renvoyé à la ligne pour le paragraphe actuel. Sinon, le texte latin est renvoyé à la ligne par mots entiers.

```cpp
bool Aspose::Words::ParagraphFormat::get_WordWrap()
```


## Exemples



Montre comment définir des propriétés spéciales pour la typographie asiatique.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat();
format->set_FarEastLineBreakControl(true);
format->set_WordWrap(false);
format->set_HangingPunctuation(true);

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.AsianTypographyProperties.docx");
```

## Voir aussi

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
