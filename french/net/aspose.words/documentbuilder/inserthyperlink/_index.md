---
title: DocumentBuilder.InsertHyperlink
second_title: Référence de l'API Aspose.Words pour .NET
description: DocumentBuilder méthode. Insère un lien hypertexte dans le document.
type: docs
weight: 370
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
| urlOrBookmark | String | Destination du lien. Peut être une URL ou le nom d'un signet à l'intérieur du document. Cette méthode ajoute toujours des apostrophes au début et à la fin de l'URL. |
| isBookmark | Boolean | `vrai` si le paramètre précédent est le nom d'un signet à l'intérieur du document ; `FAUX` est-ce que le paramètre précédent est une URL. |

### Return_Value

UN[`Field`](../../../aspose.words.fields/field/) objet qui représente le champ inséré.

### Remarques

Notez que vous devez spécifier le formatage de la police pour le texte affiché du lien hypertexte explicitement à l'aide de l'option[`Font`](../font/) propriété.

Cette méthode appelle en interne[`InsertField`](../insertfield/) pour insérer un MS Word HYPERLINK field dans le document.

### Exemples

Montre comment insérer un lien hypertexte faisant référence à un signet local.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("Bookmark1");
builder.Write("Bookmarked text. ");
builder.EndBookmark("Bookmark1");
builder.Writeln("Text outside of the bookmark.");

// Insère un champ HYPERLINK qui renvoie au signet. Nous pouvons passer des commutateurs de terrain
// à la méthode "InsertHyperlink" dans le cadre de l'argument contenant le nom du signet référencé.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Link to Bookmark1", @"Bookmark1"" \o ""Hyperlink Tip", true);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

Montre comment insérer un champ de lien hypertexte.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// Insère un lien hypertexte et soulignez-le avec un formatage personnalisé.
// Le lien hypertexte sera un morceau de texte cliquable qui nous amènera à l'emplacement spécifié dans l'URL.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", faux);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Ctrl + clic gauche sur le lien dans le texte dans Microsoft Word nous amènera à l'URL via une nouvelle fenêtre de navigateur Web.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

Montre comment utiliser la pile de mise en forme d'un générateur de documents.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Configurez le formatage de la police, puis écrivez le texte qui précède le lien hypertexte.
builder.Font.Name = "Arial";
builder.Font.Size = 24;
builder.Write("To visit Google, hold Ctrl and click ");

// Préserve notre configuration de formatage actuelle sur la pile.
builder.PushFont();

// Modifie le formatage actuel du constructeur en appliquant un nouveau style.
builder.Font.StyleIdentifier = StyleIdentifier.Hyperlink;
builder.InsertHyperlink("here", "http://www.google.com", faux);

Assert.AreEqual(Color.Blue.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.Single, builder.Font.Underline);

// Restaurer le formatage de la police que nous avons enregistré précédemment et supprimer l'élément de la pile.
builder.PopFont();

Assert.AreEqual(Color.Empty.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.None, builder.Font.Underline);

builder.Write(". We hope you enjoyed the example.");

doc.Save(ArtifactsDir + "DocumentBuilder.PushPopFont.docx");
```

### Voir également

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../documentbuilder/)
* Assemblée [Aspose.Words](../../../)


