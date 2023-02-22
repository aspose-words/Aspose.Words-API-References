---
title: FieldMergeField.IsMapped
second_title: Référence de l'API Aspose.Words pour .NET
description: FieldMergeField propriété. Obtient ou définit si ce champ est un champ mappé.
type: docs
weight: 30
url: /fr/net/aspose.words.fields/fieldmergefield/ismapped/
---
## FieldMergeField.IsMapped property

Obtient ou définit si ce champ est un champ mappé.

```csharp
public bool IsMapped { get; set; }
```

### Exemples

Montre comment utiliser les champs MERGEFIELD pour effectuer un publipostage.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crée une table de données à utiliser comme source de données de publipostage.
DataTable table = new DataTable("Employees");
table.Columns.Add("Courtesy Title");
table.Columns.Add("First Name");
table.Columns.Add("Last Name");
table.Rows.Add("Mr.", "John", "Doe");
table.Rows.Add("Mrs.", "Jane", "Cardholder");

// Insère un MERGEFIELD avec une propriété FieldName définie sur le nom d'une colonne dans la source de données.
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Courtesy Title";
fieldMergeField.IsMapped = true;
fieldMergeField.IsVerticalFormatting = false;

// Nous pouvons appliquer du texte avant et après la valeur que ce champ accepte lors de la fusion.
fieldMergeField.TextBefore = "Dear ";
fieldMergeField.TextAfter = " ";

Assert.AreEqual(" MERGEFIELD  \"Courtesy Title\" \\m \\b \"Dear \" \\f \" \"", fieldMergeField.GetFieldCode());

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
* espace de noms [Aspose.Words.Fields](../../fieldmergefield/)
* Assemblée [Aspose.Words](../../../)


