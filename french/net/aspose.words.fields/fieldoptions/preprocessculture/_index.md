---
title: FieldOptions.PreProcessCulture
linktitle: PreProcessCulture
articleTitle: PreProcessCulture
second_title: Aspose.Words pour .NET
description: FieldOptions PreProcessCulture propriété. Obtient ou définit la culture pour prétraiter les valeurs des champs en C#.
type: docs
weight: 170
url: /fr/net/aspose.words.fields/fieldoptions/preprocessculture/
---
## FieldOptions.PreProcessCulture property

Obtient ou définit la culture pour prétraiter les valeurs des champs.

```csharp
public CultureInfo PreProcessCulture { get; set; }
```

## Remarques

Actuellement, cette propriété n'affecte que la valeur du[`FieldDocProperty`](../../fielddocproperty/) champ.

La valeur par défaut est`nul` . Lorsque cette propriété est définie sur`nul` , le[`FieldDocProperty`](../../fielddocproperty/)la valeur du champ est preprocessed avec la culture contrôlée par le[`FieldUpdateCultureSource`](../fieldupdateculturesource/) propriété.

## Exemples

Montre comment définir la culture de prétraitement.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// Définit la culture selon laquelle certains champs formateront leurs valeurs affichées.
doc.FieldOptions.PreProcessCulture = new CultureInfo("de-DE");

Field field = builder.InsertField(" DOCPROPERTY CreateTime");

// Le champ DOCPROPERTY affichera son résultat formaté selon la culture du prétraitement
// nous avons défini l'allemand. Le champ affichera la date/heure au format « jj.mm.aaaa hh:mm ».
Assert.IsTrue(Regex.Match(field.Result, @"\d{2}[.]\d{2}[.]\d{4} \d{2}[:]\d{2}").Success);

doc.FieldOptions.PreProcessCulture = CultureInfo.InvariantCulture;
field.Update();

// Après passage en culture invariante, le champ DOCPROPERTY utilisera le format "mm/jj/aaaa hh:mm".
Assert.IsTrue(Regex.Match(field.Result, @"\d{2}[/]\d{2}[/]\d{4} \d{2}[:]\d{2}").Success);
```

### Voir également

* class [FieldOptions](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
