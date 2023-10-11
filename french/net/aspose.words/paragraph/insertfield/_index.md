---
title: Paragraph.InsertField
second_title: Référence de l'API Aspose.Words pour .NET
description: Paragraph méthode. Insère un champ dans ce paragraphe.
type: docs
weight: 290
url: /fr/net/aspose.words/paragraph/insertfield/
---
## InsertField(FieldType, bool, Node, bool) {#insertfield}

Insère un champ dans ce paragraphe.

```csharp
public Field InsertField(FieldType fieldType, bool updateField, Node refNode, bool isAfter)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fieldType | FieldType | Le type du champ à insérer. |
| updateField | Boolean | Spécifie s'il faut mettre à jour le champ immédiatement. |
| refNode | Node | Noeud de référence à l'intérieur de ce paragraphe (si*refNode* est`nul`, puis ajouté à la fin du paragraphe). |
| isAfter | Boolean | S'il faut insérer le champ après ou avant le nœud de référence. |

### Return_Value

UN[`Field`](../../../aspose.words.fields/field/) objet qui représente le champ inséré.

### Exemples

Montre différentes manières d’ajouter des champs à un paragraphe.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Vous trouverez ci-dessous trois manières d'insérer un champ dans un paragraphe.
// 1 - Insère un champ AUTEUR dans un paragraphe après l'un des nœuds enfants du paragraphe :
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - Insérer un champ QUOTE après l'un des nœuds enfants du paragraphe :
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Insérer un champ QUOTE avant un des nœuds enfants du paragraphe,
// et lui faire afficher une valeur d'espace réservé :
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// Ce champ affichera sa valeur d'espace réservé jusqu'à ce que nous le mettions à jour.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### Voir également

* class [Field](../../../aspose.words.fields/field/)
* enum [FieldType](../../../aspose.words.fields/fieldtype/)
* class [Node](../../node/)
* class [Paragraph](../)
* espace de noms [Aspose.Words](../../paragraph/)
* Assemblée [Aspose.Words](../../../)

---

## InsertField(string, Node, bool) {#insertfield_1}

Insère un champ dans ce paragraphe.

```csharp
public Field InsertField(string fieldCode, Node refNode, bool isAfter)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fieldCode | String | Le code du champ à insérer (sans accolades). |
| refNode | Node | Noeud de référence à l'intérieur de ce paragraphe (si*refNode* est`nul`, puis ajouté à la fin du paragraphe). |
| isAfter | Boolean | S'il faut insérer le champ après ou avant le nœud de référence. |

### Return_Value

UN[`Field`](../../../aspose.words.fields/field/) objet qui représente le champ inséré.

### Exemples

Montre différentes manières d’ajouter des champs à un paragraphe.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Vous trouverez ci-dessous trois manières d'insérer un champ dans un paragraphe.
// 1 - Insère un champ AUTEUR dans un paragraphe après l'un des nœuds enfants du paragraphe :
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - Insérer un champ QUOTE après l'un des nœuds enfants du paragraphe :
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Insérer un champ QUOTE avant un des nœuds enfants du paragraphe,
// et lui faire afficher une valeur d'espace réservé :
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// Ce champ affichera sa valeur d'espace réservé jusqu'à ce que nous le mettions à jour.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### Voir également

* class [Field](../../../aspose.words.fields/field/)
* class [Node](../../node/)
* class [Paragraph](../)
* espace de noms [Aspose.Words](../../paragraph/)
* Assemblée [Aspose.Words](../../../)

---

## InsertField(string, string, Node, bool) {#insertfield_2}

Insère un champ dans ce paragraphe.

```csharp
public Field InsertField(string fieldCode, string fieldValue, Node refNode, bool isAfter)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fieldCode | String | Le code du champ à insérer (sans accolades). |
| fieldValue | String | La valeur du champ à insérer. Passer`nul` pour les champs qui n'ont pas de valeur. |
| refNode | Node | Noeud de référence à l'intérieur de ce paragraphe (si*refNode* est`nul`, puis ajouté à la fin du paragraphe). |
| isAfter | Boolean | S'il faut insérer le champ après ou avant le nœud de référence. |

### Return_Value

UN[`Field`](../../../aspose.words.fields/field/) objet qui représente le champ inséré.

### Exemples

Montre différentes manières d’ajouter des champs à un paragraphe.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Vous trouverez ci-dessous trois manières d'insérer un champ dans un paragraphe.
// 1 - Insère un champ AUTEUR dans un paragraphe après l'un des nœuds enfants du paragraphe :
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - Insérer un champ QUOTE après l'un des nœuds enfants du paragraphe :
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Insérer un champ QUOTE avant un des nœuds enfants du paragraphe,
// et lui faire afficher une valeur d'espace réservé :
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// Ce champ affichera sa valeur d'espace réservé jusqu'à ce que nous le mettions à jour.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### Voir également

* class [Field](../../../aspose.words.fields/field/)
* class [Node](../../node/)
* class [Paragraph](../)
* espace de noms [Aspose.Words](../../paragraph/)
* Assemblée [Aspose.Words](../../../)


