---
title: Range.UnlinkFields
linktitle: UnlinkFields
articleTitle: UnlinkFields
second_title: Aspose.Words pour .NET
description: Découvrez la méthode Range UnlinkFields pour dissocier sans effort les champs de votre plage de documents, améliorant ainsi votre flux de travail et la gestion de vos documents.
type: docs
weight: 120
url: /fr/net/aspose.words/range/unlinkfields/
---
## Range.UnlinkFields method

Dissocie les champs de cette plage.

```csharp
public void UnlinkFields()
```

## Remarques

Remplace tous les champs de cette plage par leurs résultats les plus récents.

Pour dissocier les champs dans l'ensemble du document, utilisez`UnlinkFields`.

## Exemples

Montre comment dissocier tous les champs d'une plage.

```csharp
Document doc = new Document(MyDir + "Linked fields.docx");

Section newSection = (Section)doc.Sections[0].Clone(true);
doc.Sections.Add(newSection);

doc.Sections[1].Range.UnlinkFields();
```

### Voir également

* class [Range](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
