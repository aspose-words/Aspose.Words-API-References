---
title: "Aspose::Words::ParagraphFormat::get_WidowControl méthode"
linktitle: "get_WidowControl"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::ParagraphFormat::get_WidowControl méthode. Vrai si les première et dernière lignes du paragraphe doivent rester sur la même page que le reste du paragraphe en C++."
type: docs
weight: 41000
url: /fr/cpp/aspose.words/paragraphformat/get_widowcontrol/
---
## ParagraphFormat::get_WidowControl method


Vrai si les première et dernière lignes du paragraphe doivent rester sur la même page que le reste du paragraphe.

```cpp
bool Aspose::Words::ParagraphFormat::get_WidowControl()
```


## Exemples



Montre comment activer le contrôle veuve/orphelin pour un paragraphe.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Lorsque nous écrivons le texte qui ne tient pas sur une seule page, une ligne peut déborder sur la page suivante.
// La ligne unique qui se retrouve sur la page suivante s'appelle un "Orphelin",
// et la ligne précédente où l'orphelin s'est détaché s'appelle une "Veuve".
// Nous pouvons corriger les orphelins et les veuves en réarrangeant le texte via la taille de police, l'espacement ou les marges de page.
// Si nous souhaitons préserver les dimensions de notre document, nous pouvons définir cet indicateur sur "true"
// pour pousser les veuves sur la même page que leurs orphelins respectifs.
// Laisser cet indicateur à "false" laissera les paires veuve/orphelin dans le texte.
// Chaque paragraphe possède ce paramètre accessible dans Microsoft Word via Accueil -> Paragraphe -> Paramètres du paragraphe
// (bouton en bas à droite de l'onglet "Paragraph") -> "Contrôle Veuve/Orphelin".
builder->get_ParagraphFormat()->set_WidowControl(widowControl);

// Insérez du texte qui produit un orphelin et une veuve.
builder->get_Font()->set_Size(68);
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.WidowControl.docx");
```

## Voir aussi

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
