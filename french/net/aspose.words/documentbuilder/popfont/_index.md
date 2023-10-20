---
title: DocumentBuilder.PopFont
linktitle: PopFont
articleTitle: PopFont
second_title: Aspose.Words pour .NET
description: DocumentBuilder PopFont méthode. Récupère le formatage des caractères précédemment enregistré sur la pile en C#.
type: docs
weight: 590
url: /fr/net/aspose.words/documentbuilder/popfont/
---
## DocumentBuilder.PopFont method

Récupère le formatage des caractères précédemment enregistré sur la pile.

```csharp
public void PopFont()
```

## Exemples

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

* property [Font](../font/)
* method [PushFont](../pushfont/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
