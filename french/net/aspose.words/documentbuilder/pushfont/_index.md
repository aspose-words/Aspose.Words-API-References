---
title: DocumentBuilder.PushFont
linktitle: PushFont
articleTitle: PushFont
second_title: Aspose.Words pour .NET
description: Découvrez comment la méthode DocumentBuilder PushFont améliore la mise en forme de votre document en enregistrant les styles de caractères pour une récupération facile et une conception cohérente.
type: docs
weight: 640
url: /fr/net/aspose.words/documentbuilder/pushfont/
---
## DocumentBuilder.PushFont method

Enregistre le formatage actuel des caractères sur la pile.

```csharp
public void PushFont()
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
* method [PopFont](../popfont/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
