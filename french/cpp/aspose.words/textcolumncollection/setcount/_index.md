---
title: "Aspose::Words::TextColumnCollection::SetCount méthode"
linktitle: "SetCount"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::TextColumnCollection::SetCount méthode. Dispose le texte dans le nombre spécifié de colonnes de texte en C++."
type: docs
weight: 13000
url: /fr/cpp/aspose.words/textcolumncollection/setcount/
---
## TextColumnCollection::SetCount method


Dispose le texte en le répartissant dans le nombre spécifié de colonnes de texte.

```cpp
void Aspose::Words::TextColumnCollection::SetCount(int32_t newCount)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| newCount | int32_t | Le nombre de colonnes dans lesquelles le texte doit être disposé. |
## Remarques


Lorsque [EvenlySpaced](../get_evenlyspaced/) est **false** et que vous augmentez le nombre de colonnes, de nouveaux objets [TextColumn](../../textcolumn/) sont créés avec une largeur et un espacement nuls. Vous devez définir la largeur et l’espacement pour les nouvelles colonnes.

## Exemples



Montre comment créer plusieurs colonnes espacées uniformément dans une section.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::TextColumnCollection> columns = builder->get_PageSetup()->get_TextColumns();
columns->set_Spacing(100);
columns->SetCount(2);

builder->Writeln(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");

doc->Save(get_ArtifactsDir() + u"PageSetup.ColumnsSameWidth.docx");
```

## Voir aussi

* Class [TextColumnCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
