---
title: "Aspose::Words::Saving::TxtSaveOptions::get_PreserveTableLayout méthode"
linktitle: "get_PreserveTableLayout"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::TxtSaveOptions::get_PreserveTableLayout méthode. Spécifie si le programme doit tenter de préserver la mise en page des tables lors de l'enregistrement au format texte brut. La valeur par défaut est false en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.saving/txtsaveoptions/get_preservetablelayout/
---
## TxtSaveOptions::get_PreserveTableLayout method


Spécifie si le programme doit tenter de préserver la mise en page des tableaux lors de l'enregistrement au format texte brut. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Saving::TxtSaveOptions::get_PreserveTableLayout() const
```


## Exemples



Montre comment préserver la mise en page des tables lors de la conversion en texte brut.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1");
builder->InsertCell();
builder->Write(u"Row 1, cell 2");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, cell 1");
builder->InsertCell();
builder->Write(u"Row 2, cell 2");
builder->EndTable();

// Créez un objet "TxtSaveOptions" que nous pouvons passer à la méthode "Save" du document
// pour modifier la façon dont nous enregistrons le document en texte brut.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// Définissez la propriété "PreserveTableLayout" sur "true" pour appliquer un remplissage d'espaces blancs au contenu
// du document texte brut de sortie afin de préserver autant que possible la mise en page de la table.
// Définissez la propriété "PreserveTableLayout" sur "false" pour enregistrer le contenu de toutes les tables
// en un corps de texte continu, avec simplement une nouvelle ligne pour chaque ligne.
txtSaveOptions->set_PreserveTableLayout(preserveTableLayout);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.PreserveTableLayout.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.PreserveTableLayout.txt");

if (preserveTableLayout)
{
    ASSERT_EQ(System::String(u"Row 1, cell 1                                            Row 1, cell 2\r\n") + u"Row 2, cell 1                                            Row 2, cell 2\r\n\r\n", docText);
}
else
{
    ASSERT_EQ(System::String(u"Row 1, cell 1\r") + u"Row 1, cell 2\r" + u"Row 2, cell 1\r" + u"Row 2, cell 2\r\r\n", docText);
}
```

## Voir aussi

* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
