---
title: ReportingEngine.MissingMemberMessage
linktitle: MissingMemberMessage
articleTitle: MissingMemberMessage
second_title: Aspose.Words pour .NET
description: Découvrez la propriété MissingMemberMessage de ReportingEngine et personnalisez facilement les messages pour les membres d'objet manquants. Améliorez l'expérience utilisateur sans effort !
type: docs
weight: 30
url: /fr/net/aspose.words.reporting/reportingengine/missingmembermessage/
---
## ReportingEngine.MissingMemberMessage property

Obtient ou définit une valeur de chaîne affichée à la place d'une expression de modèle représentant une simple référence à un membre manquant d'un objet. La valeur par défaut est une chaîne vide.

```csharp
public string MissingMemberMessage { get; set; }
```

## Remarques

La propriété doit être utilisée en conjonction avec leAllowMissingMembers Option . Sinon, une exception est levée lorsqu'un membre manquant d'un objet est détecté.

Cette propriété affecte uniquement l'impression d'une expression modèle représentant une référence simple à un membre d'objet missing . Par exemple, l'impression d'un opérateur binaire dont l'un des opérandes référence un membre d'objet missing n'est pas affectée.

La valeur de cette propriété ne peut pas être définie sur null.

## Exemples

Montre comment autoriser les membres manquants.

```csharp
DocumentBuilder builder = new DocumentBuilder();
builder.Writeln("<<[missingObject.First().id]>>");
builder.Writeln("<<foreach [in missingObject]>><<[id]>><</foreach>>");

ReportingEngine engine = new ReportingEngine { Options = ReportBuildOptions.AllowMissingMembers };
engine.MissingMemberMessage = "Missed";
engine.BuildReport(builder.Document, new DataSet(), "");
```

### Voir également

* class [ReportingEngine](../)
* espace de noms [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Assemblée [Aspose.Words](../../../)
