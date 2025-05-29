---
title: Paragraph.AppendField
linktitle: AppendField
articleTitle: AppendField
second_title: Aspose.Words pour .NET
description: Améliorez votre document avec la méthode Paragraph AppendField, en ajoutant de manière transparente des champs personnalisés aux paragraphes pour une meilleure organisation et clarté.
type: docs
weight: 260
url: /fr/net/aspose.words/paragraph/appendfield/
---
## AppendField(*[FieldType](../../../aspose.words.fields/fieldtype/), bool*) {#appendfield}

Ajoute un champ à ce paragraphe.

```csharp
public Field AppendField(FieldType fieldType, bool updateField)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fieldType | FieldType | Le type de champ à ajouter. |
| updateField | Boolean | Spécifie s'il faut mettre à jour le champ immédiatement. |

### Return_Value

UN[`Field`](../../../aspose.words.fields/field/) objet qui représente le champ ajouté.

## Exemples

Affiche différentes manières d’ajouter des champs à un paragraphe.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// Vous trouverez ci-dessous trois manières d’ajouter un champ à la fin d’un paragraphe.
// 1 - Ajoutez un champ DATE à l'aide d'un type de champ, puis mettez-le à jour :
paragraph.AppendField(FieldType.FieldDate, true);

 // 2 - Ajouter un champ TIME à l'aide d'un code de champ :
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 - Ajoutez un champ QUOTE à l'aide d'un code de champ et faites en sorte qu'il affiche une valeur d'espace réservé :
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.AreEqual("Placeholder value", doc.Range.Fields[2].Result);

// Ce champ affichera sa valeur d'espace réservé jusqu'à ce que nous le mettions à jour.
doc.UpdateFields();

Assert.AreEqual("Real value", doc.Range.Fields[2].Result);

doc.Save(ArtifactsDir + "Paragraph.AppendField.docx");
```

### Voir également

* class [Field](../../../aspose.words.fields/field/)
* enum [FieldType](../../../aspose.words.fields/fieldtype/)
* class [Paragraph](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## AppendField(*string*) {#appendfield_1}

Ajoute un champ à ce paragraphe.

```csharp
public Field AppendField(string fieldCode)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fieldCode | String | Le code du champ à ajouter (sans accolades). |

### Return_Value

UN[`Field`](../../../aspose.words.fields/field/) objet qui représente le champ ajouté.

## Exemples

Affiche différentes manières d’ajouter des champs à un paragraphe.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// Vous trouverez ci-dessous trois manières d’ajouter un champ à la fin d’un paragraphe.
// 1 - Ajoutez un champ DATE à l'aide d'un type de champ, puis mettez-le à jour :
paragraph.AppendField(FieldType.FieldDate, true);

 // 2 - Ajouter un champ TIME à l'aide d'un code de champ :
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 - Ajoutez un champ QUOTE à l'aide d'un code de champ et faites en sorte qu'il affiche une valeur d'espace réservé :
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.AreEqual("Placeholder value", doc.Range.Fields[2].Result);

// Ce champ affichera sa valeur d'espace réservé jusqu'à ce que nous le mettions à jour.
doc.UpdateFields();

Assert.AreEqual("Real value", doc.Range.Fields[2].Result);

doc.Save(ArtifactsDir + "Paragraph.AppendField.docx");
```

### Voir également

* class [Field](../../../aspose.words.fields/field/)
* class [Paragraph](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## AppendField(*string, string*) {#appendfield_2}

Ajoute un champ à ce paragraphe.

```csharp
public Field AppendField(string fieldCode, string fieldValue)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fieldCode | String | Le code du champ à ajouter (sans accolades). |
| fieldValue | String | La valeur du champ à ajouter. Passer`nul` pour les champs qui n'ont pas de valeur. |

### Return_Value

UN[`Field`](../../../aspose.words.fields/field/) objet qui représente le champ ajouté.

## Exemples

Affiche différentes manières d’ajouter des champs à un paragraphe.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// Vous trouverez ci-dessous trois manières d’ajouter un champ à la fin d’un paragraphe.
// 1 - Ajoutez un champ DATE à l'aide d'un type de champ, puis mettez-le à jour :
paragraph.AppendField(FieldType.FieldDate, true);

 // 2 - Ajouter un champ TIME à l'aide d'un code de champ :
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 - Ajoutez un champ QUOTE à l'aide d'un code de champ et faites en sorte qu'il affiche une valeur d'espace réservé :
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.AreEqual("Placeholder value", doc.Range.Fields[2].Result);

// Ce champ affichera sa valeur d'espace réservé jusqu'à ce que nous le mettions à jour.
doc.UpdateFields();

Assert.AreEqual("Real value", doc.Range.Fields[2].Result);

doc.Save(ArtifactsDir + "Paragraph.AppendField.docx");
```

### Voir également

* class [Field](../../../aspose.words.fields/field/)
* class [Paragraph](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
