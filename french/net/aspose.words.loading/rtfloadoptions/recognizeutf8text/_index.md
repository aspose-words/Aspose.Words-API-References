---
title: RtfLoadOptions.RecognizeUtf8Text
linktitle: RecognizeUtf8Text
articleTitle: RecognizeUtf8Text
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété RtfLoadOptions RecognizeUtf8Text préserve les caractères UTF-8 lors de l'importation, garantissant une représentation précise du texte et une intégration transparente.
type: docs
weight: 20
url: /fr/net/aspose.words.loading/rtfloadoptions/recognizeutf8text/
---
## RtfLoadOptions.RecognizeUtf8Text property

Lorsqu'il est réglé sur`vrai` , essaiera de détecter les caractères UTF8, ils seront conservés lors de l'importation.

```csharp
public bool RecognizeUtf8Text { get; set; }
```

## Remarques

La valeur par défaut est`FAUX`.

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
