---
title: ImportFormatOptions.MergePastedLists
linktitle: MergePastedLists
articleTitle: MergePastedLists
second_title: Aspose.Words pour .NET
description: ImportFormatOptions MergePastedLists propriété. Obtient ou définit une valeur booléenne qui spécifie si les listes collées seront fusionnées avec les listes environnantes. La valeur par défaut estFAUX  en C#.
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

Montre comment fusionner des listes à partir d’un document.

```csharp
Document srcDoc = new Document(MyDir + "List item.docx");
Document dstDoc = new Document(MyDir + "List destination.docx");

ImportFormatOptions options = new ImportFormatOptions { MergePastedLists = true };

// Définissez la propriété "MergePastedLists" sur "true". Les listes collées seront fusionnées avec les listes environnantes.
dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, options);

dstDoc.Save(ArtifactsDir + "Document.MergePastedLists.docx");
```

### Voir également

* class [ImportFormatOptions](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
