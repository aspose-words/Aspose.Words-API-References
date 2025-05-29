---
title: ReportingEngine.SetRestrictedTypes
linktitle: SetRestrictedTypes
articleTitle: SetRestrictedTypes
second_title: Aspose.Words pour .NET
description: Découvrez comment la méthode SetRestrictedTypes dans ReportingEngine améliore la sécurité en limitant l'accès des membres dans la syntaxe du modèle pour un reporting de données optimisé.
type: docs
weight: 80
url: /fr/net/aspose.words.reporting/reportingengine/setrestrictedtypes/
---
## ReportingEngine.SetRestrictedTypes method

Spécifie les types, les membres ainsi que les membres des types dérivés qui doivent être inaccessibles par le moteur via la syntaxe du modèle.

```csharp
public static void SetRestrictedTypes(params Type[] types)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| types | Type[] | Types à restreindre. |

## Remarques

Les types restreints doivent être définis avant la toute première génération d'un rapport. Après`Rapport de construction` Si une exception est levée, les types restreints ne peuvent pas être modifiés. Le meilleur endroit pour définir les types restreints est le démarrage de l'application.

Notez qu'un grand nombre de types restreints peut affecter les performances, il est donc préférable de restreindre uniquement ces types dont l'accès aux membres est vraiment sensible.

LancersArgumentException dans les cas suivants :

-*types* est nul.

- L'un des*types* les articles sont`nul`.

- L'un des*types* items représente un type invisible, c'est-à-dire un type non public ou un type imbriqué public qui a un type externe non public.

- L'un des*types* items représente un type de tableau.

-*types* contenir des entrées en double.

## Exemples

Montre comment refuser l'accès aux membres de types considérés comme non sécurisés.

```csharp
Document doc =
    DocumentHelper.CreateSimpleDocument(
        "<<var [typeVar = \"\".GetType().BaseType]>><<[typeVar]>>");

// Notez que vous ne pouvez pas définir de types restreints pendant ou après la création d'un rapport.
ReportingEngine.SetRestrictedTypes(typeof(System.Type));
// Nous définissons l'option « AllowMissingMembers » pour éviter les exceptions lors de la création d'un rapport.
ReportingEngine engine = new ReportingEngine() { Options = ReportBuildOptions.AllowMissingMembers };
engine.BuildReport(doc, new object());

// Nous obtenons une chaîne vide car nous ne pouvons pas accéder à la méthode GetType().
Assert.AreEqual(string.Empty, doc.GetText().Trim());
```

### Voir également

* class [ReportingEngine](../)
* espace de noms [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Assemblée [Aspose.Words](../../../)
