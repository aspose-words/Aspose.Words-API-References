---
title: Section.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words pour .NET
description: Dupliquez facilement des sections grâce à notre méthode de clonage de sections. Optimisez votre flux de travail et gagnez en productivité grâce à cet outil performant !
type: docs
weight: 130
url: /fr/net/aspose.words/section/clone/
---
## Section.Clone method

Crée un doublon de cette section.

```csharp
public Section Clone()
```

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

* class [Section](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
