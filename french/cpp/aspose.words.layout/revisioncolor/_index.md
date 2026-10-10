---
title: "Aspose::Words::Layout::RevisionColor enum"
linktitle: "RevisionColor"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Layout::RevisionColor enum. Permet de spécifier la couleur des révisions de document en C++."
type: docs
weight: 11000
url: /fr/cpp/aspose.words.layout/revisioncolor/
---
## RevisionColor enum


Permet de spécifier la couleur des révisions du document.

```cpp
enum class RevisionColor
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Auto | 0 | Par défaut. |
| Noir | 1 | Représente la couleur 000000. |
| Bleu | 2 | Représente la couleur 2e97d3. |
| VertVif | 3 | Représente la couleur 84a35b. |
| BleuClassique | 4 | Représente la couleur 0000ff. |
| RougeClassique | 5 | Représente la couleur ff0000. |
| BleuFoncé | 6 | Représente la couleur 376e96. |
| RougeFoncé | 7 | Représente la couleur 881824. |
| JauneFoncé | 8 | Représente la couleur e09a2b. |
| Gris25 | 9 | Représente la couleur a0a3a9. |
| Gray50 | 10 | Représente la couleur 50565e. |
| Green | 11 | Représente la couleur 2c6234. |
| Pink | 12 | Représente la couleur ce338f. |
| Red | 13 | Représente la couleur b5082e. |
| Teal | 14 | Représente la couleur 1b9cab. |
| Turquoise | 15 | Représente la couleur 3eafc2. |
| Violet | 16 | Représente la couleur 633277. |
| White | 17 | Représente la couleur ffffff. |
| Yellow | 18 | Représente la couleur fad272. |
| LightPink | 19 | Représente la couleur fce6f4. |
| LightBlue | 20 | Représente la couleur e1f2fa. |
| LightYellow | 21 | Représente la couleur fef4de. |
| Violet clair | 22 | Représente la couleur eadfef. |
| Orange clair | 23 | Représente la couleur fce3d0. |
| Vert clair | 24 | Représente la couleur e9f8ce. |
| Gris | 25 | Représente la couleur efeded. |
| Pas de mise en évidence | 26 | Aucune couleur n'est utilisée pour mettre en évidence les modifications de révision. |
| Par auteur | 27 | Les révisions de chaque auteur reçoivent leur propre couleur de mise en évidence à partir d'un ensemble prédéfini de couleurs à fort contraste. |


## Exemples



Montre comment modifier l'apparence des révisions dans un document de sortie rendu.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez une révision, puis changez la couleur de toutes les révisions en vert.
builder->Writeln(u"This is not a revision.");
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
builder->Writeln(u"This is a revision.");
doc->StopTrackRevisions();
builder->Writeln(u"This is not a revision.");

// Supprimez la barre qui apparaît à gauche de chaque ligne révisée.
doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertedTextColor(Aspose::Words::Layout::RevisionColor::BrightGreen);
doc->get_LayoutOptions()->get_RevisionOptions()->set_ShowRevisionBars(false);
doc->get_LayoutOptions()->get_RevisionOptions()->set_RevisionBarsPosition(Aspose::Words::Drawing::HorizontalAlignment::Right);

doc->Save(get_ArtifactsDir() + u"Revision.LayoutOptionsRevisions.pdf");
```

## Voir aussi

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
