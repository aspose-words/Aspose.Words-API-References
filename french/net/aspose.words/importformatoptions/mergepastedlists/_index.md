---
title: ImportFormatOptions.MergePastedLists
second_title: Référence de l'API Aspose.Words pour .NET
description: ImportFormatOptions propriété. Obtient ou définit une valeur booléenne qui spécifie si les listes collées seront fusionnées avec les listes environnantes. La valeur par défaut estfaux .
type: docs
weight: 60
url: /fr/net/aspose.words/importformatoptions/mergepastedlists/
---
## ImportFormatOptions.MergePastedLists property

Obtient ou définit une valeur booléenne qui spécifie si les listes collées seront fusionnées avec les listes environnantes. La valeur par défaut est`faux` .

```csharp
public bool MergePastedLists { get; set; }
```

### Exemples

Montre comment fusionner des listes à partir d'un document.

```csharp
Document srcDoc = new Document(MyDir + "List item.docx");
Document dstDoc = new Document(MyDir + "List destination.docx");

ImportFormatOptions options = new ImportFormatOptions { MergePastedLists = true };

// Définissez la propriété "MergePastedLists" sur "true" les listes collées seront fusionnées avec les listes environnantes.
dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, options);

dstDoc.Save(ArtifactsDir + "Document.MergePastedLists.docx");
```

### Voir également

* class [ImportFormatOptions](../)
* espace de noms [Aspose.Words](../../importformatoptions/)
* Assemblée [Aspose.Words](../../../)


