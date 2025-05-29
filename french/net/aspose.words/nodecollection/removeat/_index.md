---
title: NodeCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: Aspose.Words pour .NET
description: Supprimez facilement des nœuds de votre collection grâce à la méthode NodeCollection RemoveAt. Simplifiez la gestion de vos documents en supprimant rapidement des nœuds spécifiques.
type: docs
weight: 100
url: /fr/net/aspose.words/nodecollection/removeat/
---
## NodeCollection.RemoveAt method

Supprime le nœud à l'index spécifié de la collection et du document.

```csharp
public void RemoveAt(int index)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| index | Int32 | L'index de base zéro du nœud. Les index négatifs sont autorisés et indiquent l'accès depuis l'arrière de la liste. Par exemple, -1 signifie le dernier nœud, -2 signifie l'avant-dernier et ainsi de suite. |

## Exemples

Montre comment ajouter et supprimer des sections dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

Assert.AreEqual("Section 1\x000cSection 2", doc.GetText().Trim());

// Supprimez la première section du document.
doc.Sections.RemoveAt(0);

Assert.AreEqual("Section 2", doc.GetText().Trim());

// Ajoutez une copie de ce qui est maintenant la première section à la fin du document.
int lastSectionIdx = doc.Sections.Count - 1;
Section newSection = doc.Sections[lastSectionIdx].Clone();
doc.Sections.Add(newSection);

Assert.AreEqual("Section 2\x000cSection 2", doc.GetText().Trim());
```

### Voir également

* class [NodeCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
