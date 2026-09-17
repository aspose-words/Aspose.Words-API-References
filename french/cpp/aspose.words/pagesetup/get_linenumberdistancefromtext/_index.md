---
title: "Aspose::Words::PageSetup::get_LineNumberDistanceFromText méthode"
linktitle: "get_LineNumberDistanceFromText"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::PageSetup::get_LineNumberDistanceFromText méthode. Obtient ou définit la distance entre le bord droit des numéros de ligne et le bord gauche du document en C++."
type: docs
weight: 24000
url: /fr/cpp/aspose.words/pagesetup/get_linenumberdistancefromtext/
---
## PageSetup::get_LineNumberDistanceFromText method


Obtient ou définit la distance entre le bord droit des numéros de ligne et le bord gauche du document.

```cpp
double Aspose::Words::PageSetup::get_LineNumberDistanceFromText()
```


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

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
