---
title: "Méthode Aspose::Words::Lists::ListLevel::RemoveTabStop"
linktitle: "RemoveTabStop"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Lists::ListLevel::RemoveTabStop. Supprime le stop de tabulation du niveau de liste en C++."
type: docs
weight: 22500
url: /fr/cpp/aspose.words.lists/listlevel/removetabstop/
---
## ListLevel::RemoveTabStop method


Supprime le point de tabulation du niveau de liste.

```cpp
void Aspose::Words::Lists::ListLevel::RemoveTabStop()
```


## Exemples



Montre comment effacer le stop de tabulation du niveau de liste.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Créer une liste avec le formatage par défaut
builder->get_ListFormat()->ApplyNumberDefault();
builder->Writeln(u"Numbered list item 1");
builder->Writeln(u"Numbered list item 2");

// Obtenez le niveau de liste et supprimez son stop de tabulation
System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = builder->get_ListFormat()->get_ListLevel();
listLevel->RemoveTabStop();

doc->Save(get_ArtifactsDir() + u"Paragraph.RemoveTabStopFromListLevel.docx");
```

## Voir aussi

* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
