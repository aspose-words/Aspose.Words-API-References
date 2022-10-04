---
title: Update
second_title: Référence de l'API Aspose.Words pour .NET
description: Effectue la mise à jour du champ. Lance si le champ est déjà mis à jour.
type: docs
weight: 140
url: /fr/net/aspose.words.fields/field/update/
---
## Update() {#update}

Effectue la mise à jour du champ. Lance si le champ est déjà mis à jour.

```csharp
public void Update()
```

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

Montre comment formater les résultats de champ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Utilisez un générateur de document pour insérer un champ qui affiche un résultat sans format appliqué.
Field field = builder.InsertField("= 2 + 3");

Assert.AreEqual("= 2 + 3", field.GetFieldCode());
Assert.AreEqual("5", field.Result);

// Nous pouvons appliquer un format au résultat d'un champ en utilisant les propriétés du champ.
// Vous trouverez ci-dessous trois types de formats que nous pouvons appliquer au résultat d'un champ.
// 1 - Format numérique :
FieldFormat format = field.Format;
format.NumericFormat = "$###.00";
field.Update();

Assert.AreEqual("= 2 + 3 \\# $###.00", field.GetFieldCode());
Assert.AreEqual("$  5.00", field.Result);

// 2 - Format date/heure :
field = builder.InsertField("DATE");
format = field.Format;
format.DateTimeFormat = "dddd, MMMM dd, yyyy";
field.Update();

Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());
Console.WriteLine($"Today's date, in {format.DateTimeFormat} format:\n\t{field.Result}");

// 3 - Format général :
field = builder.InsertField("= 25 + 33");
format = field.Format;
format.GeneralFormats.Add(GeneralFormat.LowercaseRoman);
format.GeneralFormats.Add(GeneralFormat.Upper);
field.Update();

int index = 0;
using (IEnumerator<GeneralFormat> generalFormatEnumerator = format.GeneralFormats.GetEnumerator())
    while (generalFormatEnumerator.MoveNext())
        Console.WriteLine($"General format index {index++}: {generalFormatEnumerator.Current}");

Assert.AreEqual("= 25 + 33 \\* roman \\* Upper", field.GetFieldCode());
Assert.AreEqual("LVIII", field.Result);
Assert.AreEqual(2, format.GeneralFormats.Count);
Assert.AreEqual(GeneralFormat.LowercaseRoman, format.GeneralFormats[0]);

// Nous pouvons supprimer nos formats pour rétablir le résultat du champ dans sa forme d'origine.
format.GeneralFormats.Remove(GeneralFormat.LowercaseRoman);
format.GeneralFormats.RemoveAt(0);
Assert.AreEqual(0, format.GeneralFormats.Count);
field.Update();

Assert.AreEqual("= 25 + 33  ", field.GetFieldCode());
Assert.AreEqual("58", field.Result);
Assert.AreEqual(0, format.GeneralFormats.Count);
```

### Voir également

* class [Field](../)
* espace de noms [Aspose.Words.Fields](../../field/)
* Assemblée [Aspose.Words](../../../)

---

## Update(bool) {#update_1}

Effectue une mise à jour du champ. Lance si le champ est déjà mis à jour.

```csharp
public void Update(bool ignoreMergeFormat)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| ignoreMergeFormat | Boolean | Si`vrai` alors le formatage des résultats de champ direct est abandonné, quel que soit le commutateur MERGEFORMAT, sinon la mise à jour normale est effectuée. |

### Exemples

Montre comment conserver ou ignorer les champs INCLUDEPICTURE lors du chargement d'un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldIncludePicture includePicture = (FieldIncludePicture)builder.InsertField(FieldType.FieldIncludePicture, true);
includePicture.SourceFullName = ImageDir + "Transparent background logo.png";
includePicture.Update(true);

using (MemoryStream docStream = new MemoryStream())
{
    doc.Save(docStream, new OoxmlSaveOptions(SaveFormat.Docx));

    // Nous pouvons définir un indicateur dans un objet LoadOptions pour décider de convertir tous les champs INCLUDEPICTURE
    // dans les formes d'image lors du chargement d'un document qui les contient.
    LoadOptions loadOptions = new LoadOptions
    {
        PreserveIncludePictureField = preserveIncludePictureField
    };

    doc = new Document(docStream, loadOptions);

    if (preserveIncludePictureField)
    {
        Assert.True(doc.Range.Fields.Any(f => f.Type == FieldType.FieldIncludePicture));

        doc.UpdateFields();
        doc.Save(ArtifactsDir + "Field.PreserveIncludePicture.docx");
    }
    else
    {
        Assert.False(doc.Range.Fields.Any(f => f.Type == FieldType.FieldIncludePicture));
    }
}
```

### Voir également

* class [Field](../)
* espace de noms [Aspose.Words.Fields](../../field/)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
