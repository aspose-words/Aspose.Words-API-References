---
title: DigitalSignatureUtil.LoadSignatures
linktitle: LoadSignatures
articleTitle: LoadSignatures
second_title: Aspose.Words pour .NET
description: DigitalSignatureUtil LoadSignatures méthode. Charge les signatures numériques du document en C#.
type: docs
weight: 10
url: /fr/net/aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/
---
## LoadSignatures(*string*) {#loadsignatures_1}

Charge les signatures numériques du document.

```csharp
public static DigitalSignatureCollection LoadSignatures(string fileName)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fileName | String | Chemin d'accès au document. |

### Return_Value

Collecte de signatures numériques. Renvoie une collection vide si le fichier n'est pas signé.

## Exemples

Montre comment charger des signatures à partir d’un document signé numériquement.

```csharp
// Il existe deux manières de charger la collection de signatures numériques d'un document signé à l'aide de la classe DigitalSignatureUtil.
// 1 - Chargement à partir d'un document à partir d'un nom de fichier du système de fichiers local :
DigitalSignatureCollection digitalSignatures = 
    DigitalSignatureUtil.LoadSignatures(MyDir + "Digitally signed.docx");

// Si cette collection n'est pas vide, alors nous pouvons vérifier que le document est signé numériquement.
Assert.AreEqual(1, digitalSignatures.Count);

// 2 - Chargement depuis un document depuis un FileStream :
using (Stream stream = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    digitalSignatures = DigitalSignatureUtil.LoadSignatures(stream);
    Assert.AreEqual(1, digitalSignatures.Count);
}
```

Montre comment supprimer les signatures numériques d’un document signé numériquement.

```csharp
// Il existe deux manières d'utiliser la classe DigitalSignatureUtil pour supprimer les signatures numériques
// à partir d'un document signé en enregistrant une copie non signée de celui-ci ailleurs dans le système de fichiers local.
// 1 - Déterminez les emplacements du document signé et de la copie non signée par les chaînes de nom de fichier :
DigitalSignatureUtil.RemoveAllSignatures(MyDir + "Digitally signed.docx",
    ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx");

// 2 - Déterminez les emplacements du document signé et de la copie non signée par flux de fichiers :
using (Stream streamIn = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx", FileMode.Create))
    {
        DigitalSignatureUtil.RemoveAllSignatures(streamIn, streamOut);
    }
}

// Vérifiez que nos deux documents de sortie n'ont pas de signature numérique.
Assert.That(DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx"), Is.Empty);
Assert.That(DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx"), Is.Empty);
```

### Voir également

* class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* class [DigitalSignatureUtil](../)
* espace de noms [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* Assemblée [Aspose.Words](../../../)

---

## LoadSignatures(*Stream*) {#loadsignatures}

Charge les signatures numériques du document à l'aide de stream.

```csharp
public static DigitalSignatureCollection LoadSignatures(Stream stream)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| stream | Stream | Diffusez avec le document. |

### Return_Value

Collecte de signatures numériques. Renvoie une collection vide si le fichier n'est pas signé.

## Exemples

Montre comment charger des signatures à partir d’un document signé numériquement.

```csharp
// Il existe deux manières de charger la collection de signatures numériques d'un document signé à l'aide de la classe DigitalSignatureUtil.
// 1 - Chargement à partir d'un document à partir d'un nom de fichier du système de fichiers local :
DigitalSignatureCollection digitalSignatures = 
    DigitalSignatureUtil.LoadSignatures(MyDir + "Digitally signed.docx");

// Si cette collection n'est pas vide, alors nous pouvons vérifier que le document est signé numériquement.
Assert.AreEqual(1, digitalSignatures.Count);

// 2 - Chargement depuis un document depuis un FileStream :
using (Stream stream = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    digitalSignatures = DigitalSignatureUtil.LoadSignatures(stream);
    Assert.AreEqual(1, digitalSignatures.Count);
}
```

### Voir également

* class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* class [DigitalSignatureUtil](../)
* espace de noms [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* Assemblée [Aspose.Words](../../../)
