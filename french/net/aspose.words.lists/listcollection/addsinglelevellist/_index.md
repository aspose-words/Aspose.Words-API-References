---
title: ListCollection.AddSingleLevelList
linktitle: AddSingleLevelList
articleTitle: AddSingleLevelList
second_title: Aspose.Words pour .NET
description: Créez et ajoutez sans effort une liste à un seul niveau à votre document avec la méthode ListCollection AddSingleLevelList, améliorant ainsi l'organisation et la clarté.
type: docs
weight: 60
url: /fr/net/aspose.words.lists/listcollection/addsinglelevellist/
---
## ListCollection.AddSingleLevelList method

Crée une nouvelle liste à un seul niveau basée sur le modèle prédéfini et l'ajoute à la collection de listes dans le document.

```csharp
public List AddSingleLevelList(ListTemplate listTemplate)
```

## Exemples

Montre comment créer une nouvelle liste à niveau unique basée sur le modèle prédéfini.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
ListCollection listCollection = doc.Lists;

// Crée la liste à puces à partir du modèle BulletCircle.
List bulletedList = listCollection.AddSingleLevelList(ListTemplate.BulletCircle);

// Écrit la liste à puces dans le document résultant.
builder.Writeln("Bulleted list starts below:");
builder.ListFormat.List = bulletedList;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

// Crée la liste numérotée à partir du modèle NumberUppercaseLetterDot.
List numberedList = listCollection.AddSingleLevelList(ListTemplate.NumberUppercaseLetterDot);

// Écrit la liste numérotée dans le document résultant.
builder.Writeln("Numbered list starts below:");
builder.ListFormat.List = numberedList;
builder.Writeln("Item 1");
builder.Writeln("Item 2");

doc.Save(ArtifactsDir + "Lists.AddSingleLevelList.docx");
```

### Voir également

* class [List](../../list/)
* enum [ListTemplate](../../listtemplate/)
* class [ListCollection](../)
* espace de noms [Aspose.Words.Lists](../../../aspose.words.lists/)
* Assemblée [Aspose.Words](../../../)
