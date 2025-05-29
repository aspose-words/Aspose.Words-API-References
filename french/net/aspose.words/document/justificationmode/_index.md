---
title: Document.JustificationMode
linktitle: JustificationMode
articleTitle: JustificationMode
second_title: Aspose.Words pour .NET
description: Découvrez comment optimiser l'espacement des caractères de votre document grâce à la propriété JustificationMode. Améliorez la lisibilité et la présentation sans effort !
type: docs
weight: 240
url: /fr/net/aspose.words/document/justificationmode/
---
## Document.JustificationMode property

Obtient ou définit l'ajustement de l'espacement des caractères d'un document.

```csharp
public JustificationMode JustificationMode { get; set; }
```

## Exemples

Montre comment gérer le contrôle de l'espacement des caractères.

```csharp
Document doc = new Document(MyDir + "Document.docx");

JustificationMode justificationMode = doc.JustificationMode;
if (justificationMode == JustificationMode.Expand)
    doc.JustificationMode = JustificationMode.Compress;

doc.Save(ArtifactsDir + "Document.SetJustificationMode.docx");
```

### Voir également

* enum [JustificationMode](../../../aspose.words.settings/justificationmode/)
* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
