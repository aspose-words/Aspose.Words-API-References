---
title: InsertField
second_title: Référence de l'API Aspose.Words pour .NET
description: Insère un champ Word dans un document et met éventuellement à jour le résultat du champ.
type: docs
weight: 300
url: /fr/net/aspose.words/documentbuilder/insertfield/
---
## InsertField(FieldType, bool) {#insertfield}

Insère un champ Word dans un document et met éventuellement à jour le résultat du champ.

```csharp
public Field InsertField(FieldType fieldType, bool updateField)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fieldType | FieldType | Type de champ à ajouter. |
| updateField | Boolean | Spécifie s'il faut mettre à jour le champ immédiatement. |

### Return_Value

UN[`Field`](../../../aspose.words.fields/field/) objet qui représente le champ inséré.

### Remarques

Cette méthode insère un champ dans un document. Aspose.Words peut mettre à jour les champs de la plupart des types, mais pas tous. Pour plus de détails, voir the `InsertField` surcharge.

### Exemples

Montre comment insérer un champ dans un document à l'aide de FieldType.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère deux champs en passant un indicateur qui détermine s'il faut les mettre à jour au fur et à mesure que le générateur les insère.
// Dans certains cas, la mise à jour des champs peut être coûteuse en temps de calcul, et il peut être judicieux de différer la mise à jour.
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

    // Nous devrons mettre à jour ces champs manuellement à l'aide des méthodes de mise à jour.
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
* espace de noms [Aspose.Words](../../documentbuilder/)
* Assemblée [Aspose.Words](../../../)

---

## InsertField(string) {#insertfield_1}

Insère un champ Word dans un document et met à jour le résultat du champ.

```csharp
public Field InsertField(string fieldCode)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fieldCode | String | Le code de champ à insérer (sans les accolades). |

### Return_Value

UN[`Field`](../../../aspose.words.fields/field/) objet qui représente le champ inséré.

### Remarques

Cette méthode insère un champ dans un document et met à jour le résultat du champ immédiatement. Aspose.Words peut mettre à jour les champs de la plupart des types, mais pas tous. Pour plus de détails, voir the `InsertField` surcharge.

### Exemples

Montre comment insérer un champ dans un document à l'aide d'un code de champ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Cette surcharge de la méthode InsertField met automatiquement à jour les champs insérés.
Assert.That(DateTime.Parse(field.Result), Is.EqualTo(DateTime.Today).Within(1).Days);
```

Montre comment insérer des champs et y déplacer le curseur du générateur de document.

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

// Si nous souhaitons modifier le code de champ ou le contenu du champ à l'aide du constructeur,
// son curseur devrait être à l'intérieur d'un champ.
// Pour le placer dans un champ, nous aurions besoin d'appeler la méthode MoveTo du générateur de document
// et passez le nœud de début ou de séparation du champ comme argument.
builder.Write(" Text between our merge fields. ");

doc.Save(ArtifactsDir + "DocumentBuilder.MergeFields.docx");
```

### Voir également

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../documentbuilder/)
* Assemblée [Aspose.Words](../../../)

---

## InsertField(string, string) {#insertfield_2}

Insère un champ Word dans un document sans mettre à jour le résultat du champ.

```csharp
public Field InsertField(string fieldCode, string fieldValue)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fieldCode | String | Le code de champ à insérer (sans les accolades). |
| fieldValue | String | La valeur de champ à insérer. Passez null pour les champs qui n'ont pas de valeur. |

### Return_Value

UN[`Field`](../../../aspose.words.fields/field/) objet qui représente le champ inséré.

### Remarques

Les champs dans les documents Microsoft Word se composent d'un code de champ et d'un résultat de champ. Le code de champ est comme une formule et le résultat du champ est comme la valeur que la formule produit. Le code de champ peut également contenir des champs switchs qui sont comme des instructions supplémentaires pour effectuer une action spécifique.

Vous pouvez basculer entre l'affichage des codes de champ et des résultats dans votre document dans Microsoft Word à l'aide du raccourci clavier Alt+F9. Les codes de champ apparaissent entre accolades ( { } ).

Pour créer un champ, vous devez spécifier un type de champ, un code de champ et une valeur de champ "espace réservé". Si vous n'êtes pas sûr de la syntaxe d'un code de champ particulier, créez le champ dans Microsoft Word first et basculez pour voir son code de champ .

Aspose.Words peut calculer les résultats de champ pour la plupart des types de champs, mais cette méthode ne met pas automatiquement à jour le résultat de champ. Étant donné que le résultat du champ n'est pas calculé automatiquement, vous devez transmettre une valeur de chaîne (ou même une chaîne vide) qui sera insérée dans le résultat du champ. Cette valeur restera dans le résultat du champ en tant qu'espace réservé jusqu'à ce que le champ soit updated. Pour mettre à jour le résultat du champ, vous pouvez appeler[`Update`](../../../aspose.words.fields/field/update/)sur l'objet de terrain qui vous a été renvoyé ou[`UpdateFields`](../../document/updatefields/) pour mettre à jour les champs dans tout le document.

### Exemples

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

// Déplace le générateur de document vers l'en-tête principal de la première section,
// que chaque page de cette section affichera.
builder.MoveToSection(0);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

// Insère un champ PAGE, qui affichera le numéro de la page en cours.
builder.Write("Page ");
builder.InsertField("PAGE", "");

// Configurez la section pour que le nombre de pages que les champs PAGE affichent commencent à 5.
// Configurez également tous les champs PAGE pour afficher leurs numéros de page en chiffres romains majuscules.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.RestartPageNumbering = true;
pageSetup.PageStartingNumber = 5;
pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;

// Crée un autre en-tête principal pour la deuxième section, avec un autre champ PAGE.
builder.MoveToSection(1);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write(" - ");
builder.InsertField("PAGE", "");
builder.Write(" - ");

// Configurez la section pour que le nombre de pages que les champs PAGE affichent commence à 10.
// Configurez également tous les champs PAGE pour afficher leurs numéros de page en chiffres arabes.
pageSetup = doc.Sections[1].PageSetup;
pageSetup.PageStartingNumber = 10;
pageSetup.RestartPageNumbering = true;
pageSetup.PageNumberStyle = NumberStyle.Arabic;

doc.Save(ArtifactsDir + "PageSetup.PageNumbering.docx");
```

### Voir également

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../documentbuilder/)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
