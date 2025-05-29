---
title: DocumentBuilder.PopFont
linktitle: PopFont
articleTitle: PopFont
second_title: Aspose.Words pour .NET
description: Découvrez la méthode DocumentBuilder PopFont pour restaurer sans effort la mise en forme des caractères à partir de la pile, améliorant ainsi votre processus de création de documents.
type: docs
weight: 630
url: /fr/net/aspose.words/documentbuilder/popfont/
---
## DocumentBuilder.PopFont method

Récupère le formatage des caractères précédemment enregistré sur la pile.

```csharp
public void PopFont()
```

## Exemples

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

* property [Font](../font/)
* method [PushFont](../pushfont/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
