---
title: RtfLoadOptions
linktitle: RtfLoadOptions
articleTitle: RtfLoadOptions
second_title: Aspose.Words pour .NET
description: Découvrez le constructeur RtfLoadOptions qui initialise sans effort votre classe avec des valeurs par défaut, améliorant ainsi votre efficacité de codage et votre productivité.
type: docs
weight: 10
url: /fr/net/aspose.words.loading/rtfloadoptions/rtfloadoptions/
---
## RtfLoadOptions constructor

Initialise une nouvelle instance de cette classe avec les valeurs par défaut.

```csharp
public RtfLoadOptions()
```

## Exemples

Montre comment détecter les caractères UTF-8 lors du chargement d'un document RTF.

```csharp
// Créez un objet « RtfLoadOptions » pour modifier la façon dont nous chargeons un document RTF.
RtfLoadOptions loadOptions = new RtfLoadOptions();

// Définissez la propriété « RecognizeUtf8Text » sur « false » pour supposer que le document utilise le jeu de caractères ISO 8859-1
// et charge chaque caractère du document.
// Définissez la propriété « RecognizeUtf8Text » sur « true » pour analyser tous les caractères de longueur variable pouvant apparaître dans le texte.
loadOptions.RecognizeUtf8Text = recognizeUtf8Text;

Document doc = new Document(MyDir + "UTF-8 characters.rtf", loadOptions);

Assert.AreEqual(
    recognizeUtf8Text
        ? "“John Doe´s list of currency symbols”™\r" +
          "€, ¢, £, ¥, ¤"
        : "â€œJohn DoeÂ´s list of currency symbolsâ€\u009dâ„¢\r" +
          "â‚¬, Â¢, Â£, Â¥, Â¤",
    doc.FirstSection.Body.GetText().Trim());
```

### Voir également

* class [RtfLoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../../)
