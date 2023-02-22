---
title: DigitalSignatureUtil.RemoveAllSignatures
second_title: Référence de l'API Aspose.Words pour .NET
description: DigitalSignatureUtil méthode. Supprime toutes les signatures numériques du fichier source et écrit le fichier non signé dans le fichier de destination.
type: docs
weight: 20
url: /fr/net/aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/
---
## RemoveAllSignatures(string, string) {#removeallsignatures_1}

Supprime toutes les signatures numériques du fichier source et écrit le fichier non signé dans le fichier de destination.

```csharp
public static void RemoveAllSignatures(string srcFileName, string dstFileName)
```

### Exemples

Montre comment supprimer les signatures numériques d'un document signé numériquement.

```csharp
// Il existe deux façons d'utiliser la classe DigitalSignatureUtil pour supprimer les signatures numériques
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

* class [DigitalSignatureUtil](../)
* espace de noms [Aspose.Words.DigitalSignatures](../../digitalsignatureutil/)
* Assemblée [Aspose.Words](../../../)

---

## RemoveAllSignatures(Stream, Stream) {#removeallsignatures}

Supprime toutes les signatures numériques du document dans le flux source et écrit le document non signé dans le flux de destination.

**La sortie sera écrite au début du flux et la taille du flux sera mise à jour avec la longueur du contenu.**

```csharp
public static void RemoveAllSignatures(Stream srcStream, Stream dstStream)
```

### Exemples

Montre comment supprimer les signatures numériques d'un document signé numériquement.

```csharp
// Il existe deux façons d'utiliser la classe DigitalSignatureUtil pour supprimer les signatures numériques
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

* class [DigitalSignatureUtil](../)
* espace de noms [Aspose.Words.DigitalSignatures](../../digitalsignatureutil/)
* Assemblée [Aspose.Words](../../../)


