---
title: Font.ComplexScript
linktitle: ComplexScript
articleTitle: ComplexScript
second_title: Aspose.Words pour .NET
description: Font ComplexScript propriété. Spécifie si le contenu de cette exécution doit être traité comme un texte de script complexe indépendamment de leurs valeurs de caractères Unicode lors de la détermination du formatage de cette exécution en C#.
type: docs
weight: 80
url: /fr/net/aspose.words/font/complexscript/
---
## Font.ComplexScript property

Spécifie si le contenu de cette exécution doit être traité comme un texte de script complexe indépendamment de leurs valeurs de caractères Unicode lors de la détermination du formatage de cette exécution.

```csharp
public bool ComplexScript { get; set; }
```

## Exemples

Montre comment ajouter du texte qui est toujours traité comme un script complexe.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.ComplexScript = true;

builder.Writeln("Text treated as complex script.");

doc.Save(ArtifactsDir + "Font.ComplexScript.docx");
```

### Voir également

* class [Font](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
