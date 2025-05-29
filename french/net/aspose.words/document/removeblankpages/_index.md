---
title: Document.RemoveBlankPages
linktitle: RemoveBlankPages
articleTitle: RemoveBlankPages
second_title: Aspose.Words pour .NET
description: Améliorez sans effort vos documents avec la méthode RemoveBlankPages, en éliminant les pages vierges indésirables pour une finition soignée et professionnelle.
type: docs
weight: 700
url: /fr/net/aspose.words/document/removeblankpages/
---
## Document.RemoveBlankPages method

Supprime les pages vierges du document.

```csharp
public List<int> RemoveBlankPages()
```

### Return_Value

La liste des numéros de page a été considérée comme vide et supprimée.

## Remarques

Le document résultant ne contiendra pas de pages considérées comme vides tandis que les autres contenus, y compris la numérotation, les en-têtes/pieds de page et la mise en page générale doivent rester inchangés. Une page est considérée comme vide lorsque le corps de la page n'a pas de contenu visible, par exemple, un tableau vide sans bordures sera considéré comme invisible et donc la page sera détectée comme vide.

## Exemples

Montre comment supprimer les pages vierges du document.

```csharp
Document doc = new Document(MyDir + "Blank pages.docx");
Assert.AreEqual(2, doc.PageCount);
doc.RemoveBlankPages();
doc.UpdatePageLayout();
Assert.AreEqual(1, doc.PageCount);
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
