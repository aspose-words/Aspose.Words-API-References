---
title: FieldGreetingLine.GetFieldNames
linktitle: GetFieldNames
articleTitle: GetFieldNames
second_title: Aspose.Words pour .NET
description: Découvrez la méthode GetFieldNames dans FieldGreetingLine, qui récupère efficacement une collection de noms de champs de publipostage pour une intégration transparente des données.
type: docs
weight: 50
url: /fr/net/aspose.words.fields/fieldgreetingline/getfieldnames/
---
## FieldGreetingLine.GetFieldNames method

Renvoie une collection de noms de champs de publipostage utilisés par le champ.

```csharp
public string[] GetFieldNames()
```

## Exemples

Montre comment insérer un champ GREETINGLINE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Créez une salutation générique en utilisant un champ GREETINGLINE et du texte après.
FieldGreetingLine field = (FieldGreetingLine)builder.InsertField(FieldType.FieldGreetingLine, true);
builder.Writeln("\n\n\tThis is your custom greeting, created programmatically using Aspose Words!");

// Un champ GREETINGLINE accepte les valeurs d'une source de données lors d'un publipostage, comme un MERGEFIELD.
// Il peut également formater la manière dont les données de la source sont écrites à sa place une fois le publipostage terminé.
// La collection de noms de champs correspond aux colonnes de la source de données
// à partir de laquelle le champ prendra des valeurs.
Assert.AreEqual(0, field.GetFieldNames().Length);

// Pour remplir ce tableau, nous devons spécifier un format pour notre ligne de salutation.
field.NameFormat = "<< _BEFORE_ Dear >><< _TITLE0_ >><< _LAST0_ >><< _AFTER_ ,>> ";

// Maintenant, notre champ acceptera les valeurs de ces deux colonnes dans la source de données.
Assert.AreEqual("Courtesy Title", field.GetFieldNames()[0]);
Assert.AreEqual("Last Name", field.GetFieldNames()[1]);
Assert.AreEqual(2, field.GetFieldNames().Length);

// Cette chaîne couvrira tous les cas où les données de la table de données ne sont pas valides
// en remplaçant le nom mal formé par une chaîne.
field.AlternateText = "Sir or Madam";

// Définissez des paramètres régionaux pour formater le résultat.
field.LanguageId = new CultureInfo("en-US").LCID.ToString();

Assert.AreEqual(" GREETINGLINE  \\f \"<< _BEFORE_ Dear >><< _TITLE0_ >><< _LAST0_ >><< _AFTER_ ,>> \" \\e \"Sir or Madam\" \\l 1033", 
    field.GetFieldCode());

// Créer une table de données avec des colonnes dont les noms correspondent aux éléments
// à partir de la collection de noms de champs du champ, puis effectuez le publipostage.
DataTable table = new DataTable("Employees");
table.Columns.Add("Courtesy Title");
table.Columns.Add("First Name");
table.Columns.Add("Last Name");
table.Rows.Add("Mr.", "John", "Doe");
table.Rows.Add("Mrs.", "Jane", "Cardholder");

// Cette ligne a une valeur non valide dans la colonne Titre de courtoisie, donc notre message d'accueil sera par défaut le texte alternatif.
table.Rows.Add("", "No", "Name");

doc.MailMerge.Execute(table);

Assert.AreEqual(0, doc.Range.Fields.Count);
Assert.AreEqual("Dear Mr. Doe,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!\r" +
                "\fDear Mrs. Cardholder,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!\r" +
                "\fDear Sir or Madam,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!",
    doc.GetText().Trim());
```

### Voir également

* class [FieldGreetingLine](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
