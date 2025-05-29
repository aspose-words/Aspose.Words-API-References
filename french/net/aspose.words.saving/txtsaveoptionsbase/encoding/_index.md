---
title: TxtSaveOptionsBase.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words pour .NET
description: Découvrez comment optimiser les exportations de texte avec la propriété Encoding de TxtSaveOptionsBase. Définissez facilement les options d'encodage pour un formatage UTF-8 fluide.
type: docs
weight: 10
url: /fr/net/aspose.words.saving/txtsaveoptionsbase/encoding/
---
## TxtSaveOptionsBase.Encoding property

Spécifie l'encodage à utiliser lors de l'exportation au format texte. La valeur par défaut est**Codage.UTF8** .

```csharp
public Encoding Encoding { get; set; }
```

## Exemples

Montre comment définir l'encodage pour un document de sortie .txt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ajoutez du texte avec des caractères extérieurs au jeu de caractères ASCII.
builder.Write("À È Ì Ò Ù.");

// Créez un objet « TxtSaveOptions », que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la façon dont nous enregistrons le document en texte brut.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Vérifiez que la propriété « Encodage » contient l'encodage approprié pour le contenu de notre document.
Assert.AreEqual(System.Text.Encoding.UTF8, txtSaveOptions.Encoding);

doc.Save(ArtifactsDir + "TxtSaveOptions.Encoding.UTF8.txt", txtSaveOptions);

string docText = System.Text.Encoding.UTF8.GetString(File.ReadAllBytes(ArtifactsDir + "TxtSaveOptions.Encoding.UTF8.txt"));

Assert.AreEqual("\uFEFFÀ È Ì Ò Ù.\r\n", docText);

// L'utilisation d'un encodage inapproprié peut entraîner une perte du contenu du document.
txtSaveOptions.Encoding = System.Text.Encoding.ASCII;
doc.Save(ArtifactsDir + "TxtSaveOptions.Encoding.ASCII.txt", txtSaveOptions);
docText = System.Text.Encoding.ASCII.GetString(File.ReadAllBytes(ArtifactsDir + "TxtSaveOptions.Encoding.ASCII.txt"));

Assert.AreEqual("? ? ? ? ?.\r\n", docText);
```

### Voir également

* class [TxtSaveOptionsBase](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
