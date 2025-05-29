---
title: TxtLoadOptions
linktitle: TxtLoadOptions
articleTitle: TxtLoadOptions
second_title: Aspose.Words pour .NET
description: Découvrez le constructeur TxtLoadOptions ! Initialisez facilement avec des valeurs par défaut et optimisez votre processus de chargement de données pour des performances accrues.
type: docs
weight: 10
url: /fr/net/aspose.words.loading/txtloadoptions/txtloadoptions/
---
## TxtLoadOptions constructor

Initialise une nouvelle instance de cette classe avec les valeurs par défaut.

```csharp
public TxtLoadOptions()
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
