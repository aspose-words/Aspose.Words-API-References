---
title: Section.Clone
second_title: Référence de l'API Aspose.Words pour .NET
description: Section méthode. Crée un double de cette section.
type: docs
weight: 130
url: /fr/net/aspose.words/section/clone/
---
## Section.Clone method

Crée un double de cette section.

```csharp
public Section Clone()
```

### Exemples

Montre comment ajouter et supprimer des sections dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

Assert.AreEqual("Section 1\x000cSection 2", doc.GetText().Trim());

// Supprime la première section du document.
doc.Sections.RemoveAt(0);

Assert.AreEqual("Section 2", doc.GetText().Trim());

// Ajoute une copie de ce qui est maintenant la première section à la fin du document.
int lastSectionIdx = doc.Sections.Count - 1;
Section newSection = doc.Sections[lastSectionIdx].Clone();
doc.Sections.Add(newSection);

Assert.AreEqual("Section 2\x000cSection 2", doc.GetText().Trim());
```

### Voir également

* class [Section](../)
* espace de noms [Aspose.Words](../../section/)
* Assemblée [Aspose.Words](../../../)


