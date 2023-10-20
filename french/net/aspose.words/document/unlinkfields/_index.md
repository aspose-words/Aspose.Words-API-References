---
title: Document.UnlinkFields
linktitle: UnlinkFields
articleTitle: UnlinkFields
second_title: Aspose.Words pour .NET
description: Document UnlinkFields méthode. Dissocie les champs dans tout le document en C#.
type: docs
weight: 730
url: /fr/net/aspose.words/document/unlinkfields/
---
## Document.UnlinkFields method

Dissocie les champs dans tout le document.

```csharp
public void UnlinkFields()
```

## Remarques

Remplace tous les champs de l'ensemble du document par leurs résultats les plus récents.

Pour dissocier des champs dans une partie spécifique du document, utilisez[`UnlinkFields`](../../range/unlinkfields/).

## Exemples

Montre comment dissocier tous les champs du document.

```csharp
Document doc = new Document(MyDir + "Linked fields.docx");

doc.UnlinkFields();
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
