---
title: DigitalSignatureUtil.RemoveAllSignatures
linktitle: RemoveAllSignatures
articleTitle: RemoveAllSignatures
second_title: Aspose.Words per .NET
description: Rimuovi senza sforzo tutte le firme digitali con il metodo RemoveAllSignatures di DigitalSignatureUtil. Trasforma facilmente i tuoi file firmati in versioni pulite e non firmate!
type: docs
weight: 20
url: /it/net/aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/
---
## RemoveAllSignatures(*string, string*) {#removeallsignatures_1}

Rimuove tutte le firme digitali dal file sorgente e scrive il file non firmato nel file di destinazione.

I seguenti formati sono compatibili per la rimozione della firma digitale: Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott.

```csharp
public static void RemoveAllSignatures(string srcFileName, string dstFileName)
```

## Esempi

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

* class [DigitalSignatureUtil](../)
* spazio dei nomi [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* assemblea [Aspose.Words](../../../)

---

## RemoveAllSignatures(*Stream, Stream*) {#removeallsignatures}

Rimuove tutte le firme digitali dal documento nel flusso di origine e scrive il documento non firmato nel flusso di destinazione.

**L'output verrà scritto all'inizio del flusso e la dimensione del flusso verrà aggiornata in base alla lunghezza del contenuto.**

I seguenti formati sono compatibili per la rimozione della firma digitale: Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott.

```csharp
public static void RemoveAllSignatures(Stream srcStream, Stream dstStream)
```

## Esempi

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

* class [DigitalSignatureUtil](../)
* spazio dei nomi [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* assemblea [Aspose.Words](../../../)
