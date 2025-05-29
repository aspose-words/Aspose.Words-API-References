---
title: OleFormat.SuggestedFileName
linktitle: SuggestedFileName
articleTitle: SuggestedFileName
second_title: Aspose.Words pour .NET
description: Découvrez la propriété OleFormat SuggestedFileName pour récupérer facilement le nom de fichier recommandé pour enregistrer vos objets incorporés de manière transparente.
type: docs
weight: 130
url: /fr/net/aspose.words.drawing/oleformat/suggestedfilename/
---
## OleFormat.SuggestedFileName property

Obtient le nom de fichier suggéré pour l'objet incorporé actuel si vous souhaitez l'enregistrer dans un fichier.

```csharp
public string SuggestedFileName { get; }
```

## Exemples

Montre comment obtenir le nom de fichier suggéré d'un objet OLE.

```csharp
Document doc = new Document(MyDir + "OLE shape.rtf");

Shape oleShape = (Shape)doc.FirstSection.Body.GetChild(NodeType.Shape, 0, true);

// Les objets OLE peuvent fournir un nom de fichier et une extension suggérés,
// que nous pouvons utiliser lors de l'enregistrement du contenu de l'objet dans un fichier du système de fichiers local.
string suggestedFileName = oleShape.OleFormat.SuggestedFileName;

Assert.AreEqual("CSV.csv", suggestedFileName);

using (FileStream fileStream = new FileStream(ArtifactsDir + suggestedFileName, FileMode.Create))
{
    oleShape.OleFormat.Save(fileStream);
}
```

### Voir également

* class [OleFormat](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
