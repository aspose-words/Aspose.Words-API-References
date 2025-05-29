---
title: Field.Unlink
linktitle: Unlink
articleTitle: Unlink
second_title: Aspose.Words pour .NET
description: Découvrez la méthode Field Unlink pour dissocier les champs sans effort, améliorant ainsi votre gestion des données et rationalisant votre flux de travail pour des résultats optimaux.
type: docs
weight: 130
url: /fr/net/aspose.words.fields/field/unlink/
---
## Field.Unlink method

Effectue la dissociation du champ.

```csharp
public bool Unlink()
```

### Return_Value

`vrai` si le champ a été dissocié, sinon`FAUX` .

## Remarques

Remplace le champ par son résultat le plus récent.

Certains champs, tels que les champs XE (entrée d'index) et les champs SEQ (séquence), ne peuvent pas être dissociés.

## Exemples

Montre comment dissocier un champ.

```csharp
Document doc = new Document(MyDir + "Linked fields.docx");
doc.Range.Fields[1].Unlink();
```

### Voir également

* class [Field](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
