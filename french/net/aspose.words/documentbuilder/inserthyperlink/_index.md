---
title: DocumentBuilder.InsertHyperlink
linktitle: InsertHyperlink
articleTitle: InsertHyperlink
second_title: Aspose.Words pour .NET
description: Améliorez vos documents avec la méthode InsertHyperlink de DocumentBuilder, en ajoutant sans effort des liens cliquables pour une navigation et un engagement utilisateur améliorés.
type: docs
weight: 390
url: /fr/net/aspose.words/documentbuilder/inserthyperlink/
---
## DocumentBuilder.InsertHyperlink method

Insère un lien hypertexte dans le document.

```csharp
public Field InsertHyperlink(string displayText, string urlOrBookmark, bool isBookmark)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| displayText | String | Texte du lien à afficher dans le document. |
| urlOrBookmark | String | Destination du lien. Peut être une URL ou le nom d'un signet dans le document. Cette méthode ajoute toujours des apostrophes au début et à la fin de l'URL. |
| isBookmark | Boolean | `vrai` si le paramètre précédent est le nom d'un signet à l'intérieur du document ; `FAUX` le paramètre précédent est une URL. |

### Return_Value

UN[`Field`](../../../aspose.words.fields/field/) objet qui représente le champ inséré.

## Remarques

Notez que vous devez spécifier explicitement la mise en forme de la police pour le texte d'affichage du lien hypertexte en utilisant le[`Font`](../font/) propriété.

Cette méthode appelle en interne[`InsertField`](../insertfield/)pour insérer un champ HYPERLINK MS Word dans le document.

## Exemples

Montre comment insérer un champ d'hyperlien.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// Insérez un lien hypertexte et mettez-le en valeur avec une mise en forme personnalisée.
// L'hyperlien sera un morceau de texte cliquable qui nous mènera à l'emplacement spécifié dans l'URL.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", faux);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Ctrl + clic gauche sur le lien dans le texte dans Microsoft Word nous amènera à l'URL via une nouvelle fenêtre de navigateur Web.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

Montre comment insérer un lien hypertexte qui fait référence à un signet local.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("Bookmark1");
builder.Write("Bookmarked text. ");
builder.EndBookmark("Bookmark1");
builder.Writeln("Text outside of the bookmark.");

// Insérer un champ HYPERLINK pointant vers le signet. Nous pouvons passer des commutateurs de champ.
// à la méthode « InsertHyperlink » dans le cadre de l'argument contenant le nom du signet référencé.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
FieldHyperlink hyperlink = (FieldHyperlink)builder.InsertHyperlink("Link to Bookmark1", "Bookmark1", true);
hyperlink.ScreenTip = "Hyperlink Tip";

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

Montre comment utiliser la pile de formatage d'un générateur de documents.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Configurez la mise en forme de la police, puis écrivez le texte qui précède l'hyperlien.
builder.Font.Name = "Arial";
builder.Font.Size = 24;
builder.Write("To visit Google, hold Ctrl and click ");

// Préserver notre configuration de formatage actuelle sur la pile.
builder.PushFont();

// Modifiez la mise en forme actuelle du générateur en appliquant un nouveau style.
builder.Font.StyleIdentifier = StyleIdentifier.Hyperlink;
builder.InsertHyperlink("here", "http://www.google.com", faux);

Assert.AreEqual(Color.Blue.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.Single, builder.Font.Underline);

// Restaurez la mise en forme de la police que nous avons enregistrée précédemment et supprimez l'élément de la pile.
builder.PopFont();

Assert.AreEqual(Color.Empty.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.None, builder.Font.Underline);

builder.Write(". We hope you enjoyed the example.");

doc.Save(ArtifactsDir + "DocumentBuilder.PushPopFont.docx");
```

### Voir également

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
