---
title: DocumentBuilder.InsertField
linktitle: InsertField
articleTitle: InsertField
second_title: Aspose.Words pour .NET
description: Améliorez vos documents avec la méthode InsertField de DocumentBuilder. Ajoutez et mettez à jour facilement des champs Word pour un contenu dynamique et des fonctionnalités améliorées.
type: docs
weight: 330
url: /fr/net/aspose.words/documentbuilder/insertfield/
---
## InsertField(*[FieldType](../../../aspose.words.fields/fieldtype/), bool*) {#insertfield}

Insère un champ Word dans un document et met éventuellement à jour le résultat du champ.

```csharp
public Field InsertField(FieldType fieldType, bool updateField)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fieldType | FieldType | Le type de champ à ajouter. |
| updateField | Boolean | Spécifie s'il faut mettre à jour le champ immédiatement. |

### Return_Value

UN[`Field`](../../../aspose.words.fields/field/) objet qui représente le champ inséré.

## Remarques

Cette méthode insère un champ dans un document. Aspose.Words peut mettre à jour la plupart des types de champs, mais pas tous. Pour plus de détails, consultez la section « Aspose.Words ».`InsertField` surcharge.

## Exemples

Montre comment insérer un champ dans un document à l'aide de FieldType.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer deux champs tout en passant un indicateur qui détermine s'il faut les mettre à jour lorsque le générateur les insère.
// Dans certains cas, la mise à jour des champs peut être coûteuse en termes de calcul, et il peut être judicieux de différer la mise à jour.
doc.BuiltInDocumentProperties.Author = "John Doe";
builder.Write("This document was written by ");
builder.InsertField(FieldType.FieldAuthor, updateInsertedFieldsImmediately);

builder.InsertParagraph();
builder.Write("\nThis is page ");
builder.InsertField(FieldType.FieldPage, updateInsertedFieldsImmediately);

Assert.AreEqual(" AUTHOR ", doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(" PAGE ", doc.Range.Fields[1].GetFieldCode());

if (updateInsertedFieldsImmediately)
{
    Assert.AreEqual("John Doe", doc.Range.Fields[0].Result);
    Assert.AreEqual("1", doc.Range.Fields[1].Result);
}
else
{
    Assert.AreEqual(string.Empty, doc.Range.Fields[0].Result);
    Assert.AreEqual(string.Empty, doc.Range.Fields[1].Result);

    // Nous devrons mettre à jour ces champs en utilisant les méthodes de mise à jour manuellement.
    doc.Range.Fields[0].Update();

    Assert.AreEqual("John Doe", doc.Range.Fields[0].Result);

    doc.UpdateFields();

    Assert.AreEqual("1", doc.Range.Fields[1].Result);
}
```

### Voir également

* class [Field](../../../aspose.words.fields/field/)
* enum [FieldType](../../../aspose.words.fields/fieldtype/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## InsertField(*string*) {#insertfield_1}

Insère un champ Word dans un document et met à jour le résultat du champ.

```csharp
public Field InsertField(string fieldCode)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fieldCode | String | Le code du champ à insérer (sans accolades). |

### Return_Value

UN[`Field`](../../../aspose.words.fields/field/) objet qui représente le champ inséré.

## Remarques

Cette méthode insère un champ dans un document et met à jour le résultat immédiatement. Aspose.Words peut mettre à jour la plupart des types de champs, mais pas tous. Pour plus de détails, consultez la section « Aspose.Words ».`InsertField` surcharge.

## Exemples

Montre comment insérer un champ dans un document à l'aide d'un code de champ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Cette surcharge de la méthode InsertField met automatiquement à jour les champs insérés.
Assert.True((DateTime.Today - DateTime.Parse(field.Result)).Days <= 1);
```

Montre comment insérer des champs et déplacer le curseur du générateur de documents vers eux.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField(@"MERGEFIELD MyMergeField1 \* MERGEFORMAT");
builder.InsertField(@"MERGEFIELD MyMergeField2 \* MERGEFORMAT");

// Déplacez le curseur vers le premier MERGEFIELD.
builder.MoveToMergeField("MyMergeField1", true, false);

// Notez que le curseur est placé immédiatement après le premier MERGEFIELD et avant le second.
Assert.AreEqual(doc.Range.Fields[1].Start, builder.CurrentNode);
Assert.AreEqual(doc.Range.Fields[0].End, builder.CurrentNode.PreviousSibling);

// Si nous souhaitons modifier le code ou le contenu du champ à l'aide du générateur,
// son curseur devrait être à l'intérieur d'un champ.
// Pour le placer dans un champ, nous devrions appeler la méthode MoveTo du générateur de documents
// et passez le nœud de début ou de séparation du champ comme argument.
builder.Write(" Text between our merge fields. ");

doc.Save(ArtifactsDir + "DocumentBuilder.MergeFields.docx");
```

### Voir également

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## InsertField(*string, string*) {#insertfield_2}

Insère un champ Word dans un document sans mettre à jour le résultat du champ.

```csharp
public Field InsertField(string fieldCode, string fieldValue)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fieldCode | String | Le code du champ à insérer (sans accolades). |
| fieldValue | String | La valeur du champ à insérer. Passer`nul` pour les champs qui n'ont pas de valeur. |

### Return_Value

UN[`Field`](../../../aspose.words.fields/field/) objet qui représente le champ inséré.

## Remarques

Les champs des documents Microsoft Word se composent d'un code et d'un résultat. Le code est comparable à une formule et le résultat correspond à la valeur générée par la formule. Le code peut également contenir des commutateurs, qui sont comme des instructions supplémentaires pour effectuer une action spécifique.

Vous pouvez basculer entre l'affichage des codes de champ et des résultats dans votre document Microsoft Word à l'aide du raccourci clavier Alt+F9. Les codes de champ apparaissent entre accolades ({}).

Pour créer un champ, vous devez spécifier un type de champ, un code de champ et une valeur de champ « espace réservé ». Si vous n'êtes pas sûr de la syntaxe d'un code de champ particulier, créez d'abord le champ dans Microsoft Word et passez à l'affichage de son code de champ.

Aspose.Words peut calculer les résultats de la plupart des types de champs, mais cette méthode ne met pas à jour automatiquement le résultat. Comme le résultat n'est pas calculé automatiquement, vous devez lui transmettre une chaîne de caractères (voire une chaîne vide) qui sera insérée dans le résultat. Cette valeur restera dans le résultat comme espace réservé jusqu'à sa mise à jour. Pour mettre à jour le résultat, vous pouvez appeler[`Update`](../../../aspose.words.fields/field/update/) sur l'objet de terrain renvoyé à vous ou[`UpdateFields`](../../document/updatefields/) pour mettre à jour les champs dans l'ensemble du document.

## Exemples

Montre comment configurer la numérotation des pages dans une section.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1, page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 1, page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 1, page 3.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("Section 2, page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 2, page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 2, page 3.");

// Déplacer le générateur de documents vers l'en-tête principal de la première section,
// que chaque page de cette section affichera.
builder.MoveToSection(0);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

// Insérer un champ PAGE, qui affichera le numéro de la page actuelle.
builder.Write("Page ");
builder.InsertField("PAGE", "");

// Configurez la section pour que le nombre de pages affiché par les champs PAGE commence à 5.
// Configurez également tous les champs PAGE pour afficher leurs numéros de page à l'aide de chiffres romains majuscules.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.RestartPageNumbering = true;
pageSetup.PageStartingNumber = 5;
pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;

// Créez un autre en-tête principal pour la deuxième section, avec un autre champ PAGE.
builder.MoveToSection(1);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write(" - ");
builder.InsertField("PAGE", "");
builder.Write(" - ");

// Configurez la section pour que le nombre de pages affiché par les champs PAGE commence à 10.
// Configurez également tous les champs PAGE pour afficher leurs numéros de page à l'aide de chiffres arabes.
pageSetup = doc.Sections[1].PageSetup;
pageSetup.PageStartingNumber = 10;
pageSetup.RestartPageNumbering = true;
pageSetup.PageNumberStyle = NumberStyle.Arabic;

doc.Save(ArtifactsDir + "PageSetup.PageNumbering.docx");
```

### Voir également

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
