---
title: Section.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words pour .NET
description: Section Accept méthode. Accepte un visiteur en C#.
type: docs
weight: 70
url: /fr/net/aspose.words/section/accept/
---
## Section.Accept method

Accepte un visiteur.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| visitor | DocumentVisitor | Le visiteur qui visitera les nœuds. |

### Return_Value

Vrai si tous les nœuds ont été visités ; faux si[`DocumentVisitor`](../../documentvisitor/) arrêté l'opération avant de visiter tous les nœuds.

## Remarques

Énumère ce nœud et tous ses enfants. Chaque nœud appelle une méthode correspondante sur[`DocumentVisitor`](../../documentvisitor/).

Pour plus d’informations, consultez le modèle de conception Visiteur.

Appels[`VisitSectionStart`](../../documentvisitor/visitsectionstart/) , puis appelle[`Accept`](../../node/accept/) pour tous les nœuds enfants de la section et des appels[`VisitSectionEnd`](../../documentvisitor/visitsectionend/) à la fin.

### Voir également

* class [DocumentVisitor](../../documentvisitor/)
* class [Section](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
