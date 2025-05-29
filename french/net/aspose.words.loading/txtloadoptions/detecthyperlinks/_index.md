---
title: TxtLoadOptions.DetectHyperlinks
linktitle: DetectHyperlinks
articleTitle: DetectHyperlinks
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété DetectHyperlinks de TxtLoadOptions optimise le traitement de texte en détectant les hyperliens, améliorant ainsi la précision des données. La valeur par défaut est false.
type: docs
weight: 30
url: /fr/net/aspose.words.loading/txtloadoptions/detecthyperlinks/
---
## TxtLoadOptions.DetectHyperlinks property

Spécifie soit de détecter les hyperliens dans le texte. La valeur par défaut est`FAUX` .

```csharp
public bool DetectHyperlinks { get; set; }
```

## Exemples

Montre comment lire et afficher les hyperliens.

```csharp
const string inputText = "Some links in TXT:\n" +
        "https://www.aspose.com/\n" +
        "https://docs.aspose.com/words/net/\n";

using (Stream stream = new MemoryStream())
{
    byte[] buf = Encoding.ASCII.GetBytes(inputText);
    stream.Write(buf, 0, buf.Length);

    // Charger le document avec des hyperliens.
    Document doc = new Document(stream, new TxtLoadOptions() { DetectHyperlinks = true });

    // Imprimer le texte des hyperliens.
    foreach (Field field in doc.Range.Fields)
        Console.WriteLine(field.Result);

    Assert.AreEqual(doc.Range.Fields[0].Result.Trim(), "https://www.aspose.com/");
    Assert.AreEqual(doc.Range.Fields[1].Result.Trim(), "https://docs.aspose.com/words/net/");
}
```

### Voir également

* class [TxtLoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../../)
