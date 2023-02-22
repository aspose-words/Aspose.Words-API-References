---
title: Document.UpdateFields
second_title: Référence de l'API Aspose.Words pour .NET
description: Document méthode. Met à jour les valeurs des champs dans tout le document.
type: docs
weight: 730
url: /fr/net/aspose.words/document/updatefields/
---
## Document.UpdateFields method

Met à jour les valeurs des champs dans tout le document.

```csharp
public void UpdateFields()
```

### Remarques

Lorsque vous ouvrez, modifiez puis enregistrez un document, Aspose.Words ne met pas automatiquement à jour les champs, il les conserve intacts. Par conséquent, vous souhaiterez généralement appeler cette méthode avant d'enregistrer si vous avez modifié le document par programme et que vous voulez vous assurer les valeurs de champ appropriées (calculées) apparaissent dans le document enregistré.

Il n'est pas nécessaire de mettre à jour les champs après l'exécution d'un publipostage car le publipostage est une sorte de champ update et met automatiquement à jour tous les champs du document.

Cette méthode ne met pas à jour tous les types de champs. Pour la liste détaillée des types de champs pris en charge, consultez le Guide du programmeur.

Cette méthode ne met pas à jour les champs liés aux algorithmes de mise en page (par exemple, PAGE, PAGES, PAGEREF). Les champs liés à la mise en page sont mis à jour lorsque vous affichez un document ou appelez[`UpdatePageLayout`](../updatepagelayout/).

Utilisez le[`NormalizeFieldTypes`](../normalizefieldtypes/) méthode avant la mise à jour des champs s'il y avait des modifications de document qui affectaient les types de champs.

Pour mettre à jour des champs dans une partie spécifique du document, utilisez[`UpdateFields`](../../range/updatefields/).

### Exemples

Indique d'utiliser le champ QUOTE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère un champ QUOTE, qui affichera la valeur de sa propriété Text.
FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
field.Text = "\"Quoted text\"";

Assert.AreEqual(" QUOTE  \"\\\"Quoted text\\\"\"", field.GetFieldCode());

// Insère un champ QUOTE et imbrique un champ DATE à l'intérieur.
// Les champs DATE mettent à jour leur valeur à la date actuelle chaque fois que nous ouvrons le document à l'aide de Microsoft Word.
// L'imbrication du champ DATE dans le champ QUOTE comme ceci gèlera sa valeur
// à la date à laquelle nous avons créé le document.
builder.Write("\nDocument creation date: ");
field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
builder.MoveTo(field.Separator);
builder.InsertField(FieldType.FieldDate, true);

Assert.AreEqual(" QUOTE \u0013 DATE \u0014" + DateTime.Now.Date.ToShortDateString() + "\u0015", field.GetFieldCode());

// Met à jour tous les champs pour afficher leurs résultats corrects.
doc.UpdateFields();

Assert.AreEqual("\"Quoted text\"", doc.Range.Fields[0].Result);

doc.Save(ArtifactsDir + "Field.QUOTE.docx");
```

Montre comment définir les détails de l'utilisateur et les afficher à l'aide de champs.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crée un objet UserInformation et le définit comme source de données pour les champs qui affichent des informations sur l'utilisateur.
UserInformation userInformation = new UserInformation
{
    Name = "John Doe",
    Initials = "J. D.",
    Address = "123 Main Street"
};
doc.FieldOptions.CurrentUser = userInformation;

// Insérez les champs USERNAME, USERINITIALS et USERADDRESS, qui affichent les valeurs de
// les propriétés respectives de l'objet UserInformation que nous avons créé ci-dessus. 
Assert.AreEqual(userInformation.Name, builder.InsertField(" USERNAME ").Result);
Assert.AreEqual(userInformation.Initials, builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual(userInformation.Address, builder.InsertField(" USERADDRESS ").Result);

// L'objet d'options de champ a également un utilisateur statique par défaut auquel les champs de tous les documents peuvent se référer.
UserInformation.DefaultUser.Name = "Default User";
UserInformation.DefaultUser.Initials = "D. U.";
UserInformation.DefaultUser.Address = "One Microsoft Way";
doc.FieldOptions.CurrentUser = UserInformation.DefaultUser;

Assert.AreEqual("Default User", builder.InsertField(" USERNAME ").Result);
Assert.AreEqual("D. U.", builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual("One Microsoft Way", builder.InsertField(" USERADDRESS ").Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.CurrentUser.docx");
```

Montre comment insérer une table des matières (TOC) dans un document en utilisant des styles de titre comme entrées.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère une table des matières pour la première page du document.
// Configurer le tableau pour récupérer les paragraphes avec des titres de niveaux 1 à 3.
// De plus, définissez ses entrées comme étant des hyperliens qui nous mèneront
// à l'emplacement de l'en-tête lors d'un clic gauche dans Microsoft Word.
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Remplir la table des matières en ajoutant des paragraphes avec des styles de titre.
// Chacun de ces titres avec un niveau compris entre 1 et 3 créera une entrée dans la table.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 2");
builder.Writeln("Heading 3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;
builder.Writeln("Heading 3.1.1");
builder.Writeln("Heading 3.1.2");
builder.Writeln("Heading 3.1.3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;
builder.Writeln("Heading 3.1.3.1");
builder.Writeln("Heading 3.1.3.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.2");
builder.Writeln("Heading 3.3");

// Une table des matières est un champ d'un type qui doit être mis à jour pour afficher un résultat à jour.
doc.UpdateFields();
doc.Save(ArtifactsDir + "DocumentBuilder.InsertToc.docx");
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../document/)
* Assemblée [Aspose.Words](../../../)


