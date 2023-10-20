---
title: FieldGreetingLine.NameFormat
linktitle: NameFormat
articleTitle: NameFormat
second_title: Aspose.Words pour .NET
description: FieldGreetingLine NameFormat propriété. Obtient ou définit le format du nom inclus dans le champ en C#.
type: docs
weight: 40
url: /fr/net/aspose.words.fields/fieldgreetingline/nameformat/
---
## FieldGreetingLine.NameFormat property

Obtient ou définit le format du nom inclus dans le champ.

```csharp
public string NameFormat { get; set; }
```

## Exemples

Montre comment insérer un champ GREETINGLINE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crée un message d'accueil générique en utilisant un champ GREETINGLINE et du texte après celui-ci.
FieldGreetingLine field = (FieldGreetingLine)builder.InsertField(FieldType.FieldGreetingLine, true);
builder.Writeln("\n\n\tThis is your custom greeting, created programmatically using Aspose Words!");

// Un champ GREETINGLINE accepte les valeurs d'une source de données lors d'un publipostage, comme un MERGEFIELD.
// Il peut également formater la manière dont les données de la source sont écrites à leur place une fois le publipostage terminé.
// La collection des noms de champs correspond aux colonnes de la source de données
// dont le champ prendra les valeurs.
Assert.AreEqual(0, field.GetFieldNames().Length);

// Pour remplir ce tableau, nous devons spécifier un format pour notre ligne de salutation.
field.NameFormat = "<< _BEFORE_ Dear >><< _TITLE0_ >><< _LAST0_ >><< _AFTER_ ,>> ";

// Désormais, notre champ acceptera les valeurs de ces deux colonnes dans la source de données.
Assert.AreEqual("Courtesy Title", field.GetFieldNames()[0]);
Assert.AreEqual("Last Name", field.GetFieldNames()[1]);
Assert.AreEqual(2, field.GetFieldNames().Length);

// Cette chaîne couvrira tous les cas où les données de la table de données ne sont pas valides
// en remplaçant le nom mal formé par une chaîne.
field.AlternateText = "Sir or Madam";

// Définit une locale pour formater le résultat.
field.LanguageId = new CultureInfo("en-US").LCID.ToString();

Assert.AreEqual(" GREETINGLINE  \\f \"<< _BEFORE_ Dear >><< _TITLE0_ >><< _LAST0_ >><< _AFTER_ ,>> \" \\e \"Sir or Madam\" \\l 1033", 
    field.GetFieldCode());

// Crée une table de données avec des colonnes dont les noms correspondent aux éléments
// à partir de la collection de noms de champs du champ, puis réalise le publipostage.
DataTable table = new DataTable("Employees");
table.Columns.Add("Courtesy Title");
table.Columns.Add("First Name");
table.Columns.Add("Last Name");
table.Rows.Add("Mr.", "John", "Doe");
table.Rows.Add("Mrs.", "Jane", "Cardholder");

// Cette ligne a une valeur non valide dans la colonne Titre de courtoisie, donc notre message d'accueil utilisera par défaut le texte alternatif.
table.Rows.Add("", "No", "Name");

doc.MailMerge.Execute(table);

Assert.That(doc.Range.Fields, Is.Empty);
Assert.AreEqual("Dear Mr. Doe,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!\r" +
                "\fDear Mrs. Cardholder,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!\r" +
                "\fDear Sir or Madam,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!",
    doc.GetText().Trim());
```

### Voir également

* class [FieldGreetingLine](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
