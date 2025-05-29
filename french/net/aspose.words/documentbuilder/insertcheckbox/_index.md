---
title: DocumentBuilder.InsertCheckBox
linktitle: InsertCheckBox
articleTitle: InsertCheckBox
second_title: Aspose.Words pour .NET
description: Ajoutez sans effort des champs de formulaire de case à cocher interactifs avec la méthode DocumentBuilder InsertCheckBox, améliorant ainsi l'engagement des utilisateurs dans vos documents.
type: docs
weight: 290
url: /fr/net/aspose.words/documentbuilder/insertcheckbox/
---
## InsertCheckBox(*string, bool, int*) {#insertcheckbox_1}

Insère un champ de formulaire de case à cocher à la position actuelle.

```csharp
public FormField InsertCheckBox(string name, bool checkedValue, int size)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| name | String | Nom du champ de formulaire. Peut être une chaîne vide. Toute valeur de plus de 20 caractères sera tronquée. |
| checkedValue | Boolean | Statut vérifié du champ de formulaire de case à cocher. |
| size | Int32 | Spécifie la taille de la case à cocher en points. Spécifiez 0 pour MS Word afin que la taille de la case à cocher soit calculée automatiquement. |

### Return_Value

Le nœud de champ de formulaire qui vient d’être inséré.

## Remarques

Si vous spécifiez un nom pour le champ de formulaire, un signet est automatiquement créé avec le même nom.

## Exemples

Montre comment insérer des cases à cocher dans le document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer des cases à cocher de différentes tailles et des statuts cochés par défaut.
builder.Write("Unchecked check box of a default size: ");
builder.InsertCheckBox(string.Empty, false, false, 0);
builder.InsertParagraph();

builder.Write("Large checked check box: ");
builder.InsertCheckBox("CheckBox_Default", true, true, 50);
builder.InsertParagraph();

// Les champs de formulaire ont une limite de longueur de nom de 20 caractères.
builder.Write("Very large checked check box: ");
builder.InsertCheckBox("CheckBox_OnlyCheckedValue", true, 100);

Assert.AreEqual("CheckBox_OnlyChecked", doc.Range.FormFields[2].Name);

// Nous pouvons interagir avec ces cases à cocher dans Microsoft Word en double-cliquant dessus.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertCheckBox.docx");
```

### Voir également

* class [FormField](../../../aspose.words.fields/formfield/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## InsertCheckBox(*string, bool, bool, int*) {#insertcheckbox}

Insère un champ de formulaire de case à cocher à la position actuelle.

```csharp
public FormField InsertCheckBox(string name, bool defaultValue, bool checkedValue, int size)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| name | String | Nom du champ de formulaire. Peut être une chaîne vide. Toute valeur de plus de 20 caractères sera tronquée. |
| defaultValue | Boolean | Valeur par défaut du champ de formulaire de case à cocher. |
| checkedValue | Boolean | Statut coché actuel du champ de formulaire de case à cocher. |
| size | Int32 | Spécifie la taille de la case à cocher en points. Spécifiez 0 pour MS Word afin que la taille de la case à cocher soit calculée automatiquement. |

### Return_Value

Le nœud de champ de formulaire qui vient d’être inséré.

## Remarques

Si vous spécifiez un nom pour le champ de formulaire, un signet est automatiquement créé avec le même nom.

## Exemples

Montre comment insérer des cases à cocher dans le document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer des cases à cocher de différentes tailles et des statuts cochés par défaut.
builder.Write("Unchecked check box of a default size: ");
builder.InsertCheckBox(string.Empty, false, false, 0);
builder.InsertParagraph();

builder.Write("Large checked check box: ");
builder.InsertCheckBox("CheckBox_Default", true, true, 50);
builder.InsertParagraph();

// Les champs de formulaire ont une limite de longueur de nom de 20 caractères.
builder.Write("Very large checked check box: ");
builder.InsertCheckBox("CheckBox_OnlyCheckedValue", true, 100);

Assert.AreEqual("CheckBox_OnlyChecked", doc.Range.FormFields[2].Name);

// Nous pouvons interagir avec ces cases à cocher dans Microsoft Word en double-cliquant dessus.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertCheckBox.docx");
```

### Voir également

* class [FormField](../../../aspose.words.fields/formfield/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
