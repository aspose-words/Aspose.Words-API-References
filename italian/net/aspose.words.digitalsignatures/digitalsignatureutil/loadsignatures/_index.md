---
title: DigitalSignatureUtil.LoadSignatures
linktitle: LoadSignatures
articleTitle: LoadSignatures
second_title: Aspose.Words per .NET
description: Carica facilmente le firme digitali dai tuoi documenti con il metodo DigitalSignatureUtil LoadSignatures. Migliora il tuo flusso di lavoro oggi stesso!
type: docs
weight: 10
url: /it/net/aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/
---
## LoadSignatures(*string*) {#loadsignatures_1}

Carica le firme digitali dal documento.

```csharp
public static DigitalSignatureCollection LoadSignatures(string fileName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fileName | String | Percorso al documento. |

### Valore di ritorno

Raccolta di firme digitali. Restituisce una raccolta vuota se il file non è firmato.

## Esempi

Mostra come caricare le firme da un documento firmato digitalmente.

```csharp
// Esistono due modi per caricare la raccolta di firme digitali di un documento firmato utilizzando la classe DigitalSignatureUtil.
// 1 - Carica un documento da un file system locale nome file:
DigitalSignatureCollection digitalSignatures = 
    DigitalSignatureUtil.LoadSignatures(MyDir + "Digitally signed.docx");

// Se questa raccolta non è vuota, possiamo verificare che il documento sia firmato digitalmente.
Assert.AreEqual(1, digitalSignatures.Count);

// 2 - Carica da un documento da un FileStream:
using (Stream stream = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    digitalSignatures = DigitalSignatureUtil.LoadSignatures(stream);
    Assert.AreEqual(1, digitalSignatures.Count);
}
```

Mostra come rimuovere le firme digitali da un documento firmato digitalmente.

```csharp
// Esistono due modi per utilizzare la classe DigitalSignatureUtil per rimuovere le firme digitali
// da un documento firmato salvandone una copia non firmata in un'altra posizione nel file system locale.
// 1 - Determina le posizioni sia del documento firmato che della copia non firmata tramite stringhe di nomi file:
DigitalSignatureUtil.RemoveAllSignatures(MyDir + "Digitally signed.docx",
    ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx");

// 2 - Determinare le posizioni sia del documento firmato che della copia non firmata tramite flussi di file:
using (Stream streamIn = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx", FileMode.Create))
    {
        DigitalSignatureUtil.RemoveAllSignatures(streamIn, streamOut);
    }
}

// Verifichiamo che entrambi i documenti di output non abbiano firme digitali.
Assert.AreEqual(0, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx").Count);
Assert.AreEqual(0, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx").Count);
```

### Guarda anche

* class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* class [DigitalSignatureUtil](../)
* spazio dei nomi [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* assemblea [Aspose.Words](../../../)

---

## LoadSignatures(*Stream*) {#loadsignatures}

Carica le firme digitali dal documento utilizzando il flusso.

```csharp
public static DigitalSignatureCollection LoadSignatures(Stream stream)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| stream | Stream | Trasmetti in streaming con il documento. |

### Valore di ritorno

Raccolta di firme digitali. Restituisce una raccolta vuota se il file non è firmato.

## Esempi

Mostra come caricare le firme da un documento firmato digitalmente.

```csharp
// Esistono due modi per caricare la raccolta di firme digitali di un documento firmato utilizzando la classe DigitalSignatureUtil.
// 1 - Carica un documento da un file system locale nome file:
DigitalSignatureCollection digitalSignatures = 
    DigitalSignatureUtil.LoadSignatures(MyDir + "Digitally signed.docx");

// Se questa raccolta non è vuota, possiamo verificare che il documento sia firmato digitalmente.
Assert.AreEqual(1, digitalSignatures.Count);

// 2 - Carica da un documento da un FileStream:
using (Stream stream = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    digitalSignatures = DigitalSignatureUtil.LoadSignatures(stream);
    Assert.AreEqual(1, digitalSignatures.Count);
}
```

### Guarda anche

* class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* class [DigitalSignatureUtil](../)
* spazio dei nomi [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* assemblea [Aspose.Words](../../../)
