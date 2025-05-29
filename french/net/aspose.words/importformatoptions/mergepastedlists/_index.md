---
title: ImportFormatOptions.MergePastedLists
linktitle: MergePastedLists
articleTitle: MergePastedLists
second_title: Aspose.Words pour .NET
description: Fusion de listes de contrôle avec la propriété MergePastedLists de ImportFormatOptions. Gérez facilement les listes collées pour améliorer la mise en forme des documents. Valeur par défaut : false.
type: docs
weight: 70
url: /fr/net/aspose.words/importformatoptions/mergepastedlists/
---
## ImportFormatOptions.MergePastedLists property

Obtient ou définit une valeur booléenne qui spécifie si les listes collées seront fusionnées avec les listes environnantes. La valeur par défaut est`FAUX` .

```csharp
public bool MergePastedLists { get; set; }
```

## Exemples

Montre comment fusionner des listes à partir d'un document.

```csharp
Document srcDoc = new Document(MyDir + "List item.docx");
Document dstDoc = new Document(MyDir + "List destination.docx");

ImportFormatOptions options = new ImportFormatOptions { MergePastedLists = true };

// Définissez la propriété « MergePastedLists » sur « true », les listes collées seront fusionnées avec les listes environnantes.
dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, options);

dstDoc.Save(ArtifactsDir + "Document.MergePastedLists.docx");
```

### Voir également

* class [ImportFormatOptions](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
