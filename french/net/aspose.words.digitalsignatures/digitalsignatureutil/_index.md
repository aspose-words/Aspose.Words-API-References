---
title: DigitalSignatureUtil Class
linktitle: DigitalSignatureUtil
articleTitle: DigitalSignatureUtil
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.DigitalSignatures.DigitalSignatureUtil pour signer facilement vos documents avec des signatures numériques sécurisées. Améliorez l'intégrité de vos documents dès aujourd'hui !
type: docs
weight: 610
url: /fr/net/aspose.words.digitalsignatures/digitalsignatureutil/
---
## DigitalSignatureUtil class

Fournit des méthodes pour signer des documents.

Pour en savoir plus, visitez le[Travailler avec des signatures numériques](https://docs.aspose.com/words/net/working-with-digital-signatures/) article de documentation.

```csharp
public static class DigitalSignatureUtil
```

## Méthodes

| Nom | La description |
| --- | --- |
| static [LoadSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/#loadsignatures)(*Stream*) | Charge les signatures numériques du document à l'aide du flux. |
| static [LoadSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/#loadsignatures_1)(*string*) | Charge les signatures numériques du document. |
| static [RemoveAllSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/#removeallsignatures)(*Stream, Stream*) | Supprime toutes les signatures numériques du document dans le flux source et écrit le document non signé dans le flux de destination. |
| static [RemoveAllSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/#removeallsignatures_1)(*string, string*) | Supprime toutes les signatures numériques du fichier source et écrit le fichier non signé dans le fichier de destination. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign)(*Stream, Stream, [CertificateHolder](../certificateholder/)*) | Signe le document source en utilisant les données[`CertificateHolder`](../certificateholder/) avec signature numérique et écrit le document signé dans le flux de destination. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_2)(*string, string, [CertificateHolder](../certificateholder/)*) | Signe le document source en utilisant les données[`CertificateHolder`](../certificateholder/) avec signature numérique et écrit le document signé dans le fichier de destination. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_1)(*Stream, Stream, [CertificateHolder](../certificateholder/), [SignOptions](../signoptions/)*) | Signe le document source en utilisant les données[`CertificateHolder`](../certificateholder/) et[`SignOptions`](../signoptions/) avec signature numérique et écrit le document signé dans le flux de destination. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_3)(*string, string, [CertificateHolder](../certificateholder/), [SignOptions](../signoptions/)*) | Signe le document source en utilisant les données[`CertificateHolder`](../certificateholder/) et[`SignOptions`](../signoptions/) avec signature numérique et écrit le document signé dans le fichier de destination. |

## Remarques

Étant donné que la signature numérique fonctionne avec le contenu du fichier plutôt qu'avec le modèle d'objet de document, ces méthodes sont placées dans une classe distincte.

Les formats pris en charge sont : Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott.

## Exemples

Montre comment charger des signatures à partir d'un document signé numériquement.

```csharp
// Il existe deux manières de charger la collection de signatures numériques d'un document signé à l'aide de la classe DigitalSignatureUtil.
// 1 - Charger à partir d'un document à partir d'un nom de fichier du système de fichiers local :
DigitalSignatureCollection digitalSignatures = 
    DigitalSignatureUtil.LoadSignatures(MyDir + "Digitally signed.docx");

// Si cette collection n'est pas vide, nous pouvons alors vérifier que le document est signé numériquement.
Assert.AreEqual(1, digitalSignatures.Count);

// 2 - Charger à partir d'un document à partir d'un FileStream :
using (Stream stream = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    digitalSignatures = DigitalSignatureUtil.LoadSignatures(stream);
    Assert.AreEqual(1, digitalSignatures.Count);
}
```

Montre comment supprimer les signatures numériques d'un document signé numériquement.

```csharp
// Il existe deux manières d'utiliser la classe DigitalSignatureUtil pour supprimer les signatures numériques
// à partir d'un document signé en enregistrant une copie non signée de celui-ci ailleurs dans le système de fichiers local.
// 1 - Déterminer les emplacements du document signé et de la copie non signée à l'aide de chaînes de nom de fichier :
DigitalSignatureUtil.RemoveAllSignatures(MyDir + "Digitally signed.docx",
    ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx");

// 2 - Déterminer les emplacements du document signé et de la copie non signée par flux de fichiers :
using (Stream streamIn = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx", FileMode.Create))
    {
        DigitalSignatureUtil.RemoveAllSignatures(streamIn, streamOut);
    }
}

// Vérifiez que nos deux documents de sortie n'ont pas de signatures numériques.
Assert.AreEqual(0, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx").Count);
Assert.AreEqual(0, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx").Count);
```

### Voir également

* espace de noms [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* Assemblée [Aspose.Words](../../)
