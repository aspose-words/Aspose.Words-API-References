---
title: DocumentBuilder.PushFont
second_title: Référence de l'API Aspose.Words pour .NET
description: DocumentBuilder méthode. Enregistre la mise en forme actuelle des caractères sur la pile.
type: docs
weight: 570
url: /fr/net/aspose.words/documentbuilder/pushfont/
---
## DocumentBuilder.PushFont method

Enregistre la mise en forme actuelle des caractères sur la pile.

```csharp
public void PushFont()
```

### Exemples

Montre comment utiliser la pile de mise en forme d'un générateur de document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Définissez la mise en forme de la police, puis écrivez le texte qui précède le lien hypertexte.
builder.Font.Name = "Arial";
builder.Font.Size = 24;
builder.Write("To visit Google, hold Ctrl and click ");

// Préserve notre configuration de formatage actuelle sur la pile.
builder.PushFont();

// Modifie la mise en forme actuelle du générateur en appliquant un nouveau style.
builder.Font.StyleIdentifier = StyleIdentifier.Hyperlink;
builder.InsertHyperlink("here", "http://www.google.com", faux);

Assert.AreEqual(Color.Blue.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.Single, builder.Font.Underline);

// Restaure la mise en forme de la police que nous avons enregistrée précédemment et supprime l'élément de la pile.
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
* espace de noms [Aspose.Words](../../documentbuilder/)
* Assemblée [Aspose.Words](../../../)


