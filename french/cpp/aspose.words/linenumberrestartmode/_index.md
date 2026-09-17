---
title: "Enum Aspose::Words::LineNumberRestartMode"
linktitle: "LineNumberRestartMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Enum Aspose::Words::LineNumberRestartMode. Détermine quand le numérotage automatique des lignes redémarre en C++."
type: docs
weight: 94000
url: /fr/cpp/aspose.words/linenumberrestartmode/
---
## LineNumberRestartMode enum


Détermine quand le numérotage automatique des lignes redémarre.

```cpp
enum class LineNumberRestartMode
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| RestartPage | 0 | Le numérotage des lignes redémarre au début de chaque page. |
| RestartSection | 1 | Le numérotage des lignes redémarre au début de la section. |
| Continuous | 2 | Le numérotage des lignes continue à partir de la section précédente. |


## Exemples



Montre comment activer le numérotage des lignes pour une section.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Nous pouvons utiliser l'objet PageSetup de la section pour afficher les numéros à gauche des lignes de texte de la section.
// Ceci est le même comportement qu'un objet List,
// mais il couvre toute la section et ne modifie pas le texte de quelque manière que ce soit.
// Notre section redémarrera le numérotage à chaque nouvelle page à partir de 1 et affichera le numéro,
// si c'est un multiple de 3, à 50pt à gauche de la ligne.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_LineStartingNumber(1);
pageSetup->set_LineNumberCountBy(3);
pageSetup->set_LineNumberRestartMode(Aspose::Words::LineNumberRestartMode::RestartPage);
pageSetup->set_LineNumberDistanceFromText(50.0);

for (int32_t i = 1; i <= 25; i++)
{
    builder->Writeln(System::String::Format(u"Line {0}.", i));
}

// Le compteur de lignes sautera tout paragraphe dont le drapeau "SuppressLineNumbers" est réglé sur "true".
// Ce paragraphe se trouve sur la 15e ligne, qui est un multiple de 3, et afficherait donc normalement un numéro de ligne.
// Le compteur de lignes de la section ignorera également cette ligne, considérera la ligne suivante comme la 15e,
// et continuera le comptage à partir de ce point.
doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(14)->get_ParagraphFormat()->set_SuppressLineNumbers(true);

doc->Save(get_ArtifactsDir() + u"PageSetup.LineNumbers.docx");
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
