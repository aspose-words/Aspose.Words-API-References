---
title: ReportBuilderOptions.MissingMemberMessage
linktitle: MissingMemberMessage
articleTitle: MissingMemberMessage
second_title: Aspose.Words pour .NET
description: Découvrez la propriété MissingMemberMessage de ReportBuilderOptions. Personnalisez facilement les messages pour les références d'objet manquantes et améliorez ainsi l'expérience utilisateur.
type: docs
weight: 30
url: /fr/net/aspose.words.lowcode/reportbuilderoptions/missingmembermessage/
---
## ReportBuilderOptions.MissingMemberMessage property

Obtient ou définit une valeur de chaîne affichée à la place d'une expression de modèle représentant une simple référence à un membre manquant d'un objet. La valeur par défaut est une chaîne vide.

```csharp
public string MissingMemberMessage { get; set; }
```

## Remarques

La propriété doit être utilisée en conjonction avec leAllowMissingMembers Option . Sinon, une exception est levée lorsqu'un membre manquant d'un objet est détecté.

Cette propriété affecte uniquement l'impression d'une expression modèle représentant une référence simple à un membre d'objet missing . Par exemple, l'impression d'un opérateur binaire dont l'un des opérandes référence un membre d'objet missing n'est pas affectée.

La valeur de cette propriété ne peut pas être définie sur null.

### Voir également

* class [ReportBuilderOptions](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)
