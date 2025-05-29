---
title: FieldMergeField.TextAfter
linktitle: TextAfter
articleTitle: TextAfter
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FieldMergeField TextAfter pour personnaliser facilement la sortie de votre champ avec du texte dynamique, améliorant ainsi la clarté et l'engagement du document.
type: docs
weight: 50
url: /fr/net/aspose.words.fields/fieldmergefield/textafter/
---
## FieldMergeField.TextAfter property

Obtient ou définit le texte à insérer après le champ si le champ n'est pas vide.

```csharp
public string TextAfter { get; set; }
```

## Exemples

Montre comment utiliser les champs MERGEFIELD pour effectuer un publipostage.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Créez une table de données à utiliser comme source de données de publipostage.
DataTable table = new DataTable("Employees");
table.Columns.Add("Courtesy Title");
table.Columns.Add("First Name");
table.Columns.Add("Last Name");
table.Rows.Add("Mr.", "John", "Doe");
table.Rows.Add("Mrs.", "Jane", "Cardholder");

// Insérer un MERGEFIELD avec une propriété FieldName définie sur le nom d'une colonne dans la source de données.
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Courtesy Title";
fieldMergeField.IsMapped = true;
fieldMergeField.IsVerticalFormatting = false;

// Nous pouvons appliquer du texte avant et après la valeur que ce champ accepte lorsque la fusion a lieu.
fieldMergeField.TextBefore = "Dear ";
fieldMergeField.TextAfter = " ";

Assert.AreEqual(" MERGEFIELD  \"Courtesy Title\" \\m \\b \"Dear \" \\f \" \"", fieldMergeField.GetFieldCode());
Assert.AreEqual(FieldType.FieldMergeField, fieldMergeField.Type);

// Insérer un autre MERGEFIELD pour une colonne différente dans la source de données.
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Last Name";
fieldMergeField.TextAfter = ":";

doc.UpdateFields();
doc.MailMerge.Execute(table);

Assert.AreEqual("Dear Mr. Doe:\u000cDear Mrs. Cardholder:", doc.GetText().Trim());
```

### Voir également

* class [FieldMergeField](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
