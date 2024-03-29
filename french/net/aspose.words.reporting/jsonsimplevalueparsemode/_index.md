---
title: JsonSimpleValueParseMode Enum
linktitle: JsonSimpleValueParseMode
articleTitle: JsonSimpleValueParseMode
second_title: Aspose.Words pour .NET
description: Aspose.Words.Reporting.JsonSimpleValueParseMode énumération. Spécifie un mode danalyse des valeurs simples JSON null booléen nombre entier et chaîne lors du chargement de JSON. Un tel mode naffecte pas lanalyse des valeurs dateheure en C#.
type: docs
weight: 4700
url: /fr/net/aspose.words.reporting/jsonsimplevalueparsemode/
---
## JsonSimpleValueParseMode enumeration

Spécifie un mode d'analyse des valeurs simples JSON (null, booléen, nombre, entier et chaîne) lors du chargement de JSON. Un tel mode n'affecte pas l'analyse des valeurs date-heure.

```csharp
public enum JsonSimpleValueParseMode
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Loose | `0` | Spécifie le mode dans lequel les types de valeurs simples JSON sont déterminés lors de l'analyse de leurs représentations sous forme de chaîne. Par exemple, le type de 'prop' de l'extrait JSON '{ prop: "123" }' est déterminé comme un entier dans ce mode. |
| Strict | `1` | Spécifie le mode dans lequel les types de valeurs simples JSON sont déterminés à partir de la notation JSON elle-même. Par exemple, le type de 'prop' de l'extrait JSON '{ prop: "123" }' est déterminé comme chaîne dans ce mode. |

### Voir également

* espace de noms [Aspose.Words.Reporting](../../aspose.words.reporting/)
* Assemblée [Aspose.Words](../../)
