---
title: FieldEQ.AsOfficeMath
linktitle: AsOfficeMath
articleTitle: AsOfficeMath
second_title: Aspose.Words pour .NET
description: Transformez les champs EQ avec la méthode AsOfficeMath de FieldEQ, en les convertissant sans effort en objets Office Math pour une intégration transparente des documents.
type: docs
weight: 20
url: /fr/net/aspose.words.fields/fieldeq/asofficemath/
---
## FieldEQ.AsOfficeMath method

L'objet mathématique du bureau des retours correspond au champ EQ.

```csharp
public OfficeMath AsOfficeMath()
```

### Return_Value

Retours`nul` si le code du champ est vide ou invalide, sinon un[`OfficeMath`](../../../aspose.words.math/officemath/) instance.

## Exemples

Montre comment remplacer le champ EQ par Office Math.

```csharp
Document doc = new Document(MyDir + "Field sample - EQ.docx");
FieldEQ fieldEQ = doc.Range.Fields.OfType<FieldEQ>().First();

OfficeMath officeMath = fieldEQ.AsOfficeMath();

fieldEQ.Start.ParentNode.InsertBefore(officeMath, fieldEQ.Start);
fieldEQ.Remove();

doc.Save(ArtifactsDir + "Field.EQAsOfficeMath.docx");
```

### Voir également

* class [OfficeMath](../../../aspose.words.math/officemath/)
* class [FieldEQ](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
