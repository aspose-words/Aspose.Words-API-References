---
title: DigitalSignatureUtil.RemoveAllSignatures
linktitle: RemoveAllSignatures
articleTitle: RemoveAllSignatures
second_title: Aspose.Words per .NET
description: DigitalSignatureUtil RemoveAllSignatures metodo. Rimuove tutte le firme digitali dal file di origine e scrive il file non firmato nel file di destinazione in C#.
type: docs
weight: 20
url: /it/net/aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/
---
## RemoveAllSignatures(*string, string*) {#removeallsignatures_1}

Rimuove tutte le firme digitali dal file di origine e scrive il file non firmato nel file di destinazione.

I seguenti formati sono compatibili per la rimozione della firma digitale: Doc , Dot , Docx , Dotx , Docm , Odt , Ott.

```csharp
public static void RemoveAllSignatures(string srcFileName, string dstFileName)
```

## Esempi

Mostra come rimuovere le firme digitali da un documento firmato digitalmente.

```csharp
// Esistono due modi per utilizzare la classe DigitalSignatureUtil per rimuovere le firme digitali
// da un documento firmato salvandone una copia non firmata da qualche altra parte nel file system locale.
// 1 - Determina le posizioni sia del documento firmato che della copia non firmata in base alle stringhe del nome file:
DigitalSignatureUtil.RemoveAllSignatures(MyDir + "Digitally signed.docx",
    ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx");

// 2 - Determina le posizioni sia del documento firmato che della copia non firmata tramite flussi di file:
using (Stream streamIn = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx", FileMode.Create))
    {
        DigitalSignatureUtil.RemoveAllSignatures(streamIn, streamOut);
    }
}

// Verifica che entrambi i nostri documenti di output non abbiano firme digitali.
Assert.That(DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx"), Is.Empty);
Assert.That(DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx"), Is.Empty);
```

### Guarda anche

* class [DigitalSignatureUtil](../)
* spazio dei nomi [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* assemblea [Aspose.Words](../../../)

---

## RemoveAllSignatures(*Stream, Stream*) {#removeallsignatures}

Rimuove tutte le firme digitali dal documento nel flusso di origine e scrive il documento non firmato nel flusso di destinazione.

**L'output verrà scritto all'inizio dello stream e la dimensione dello stream verrà aggiornata con la lunghezza del contenuto.**

I seguenti formati sono compatibili per la rimozione della firma digitale: Doc , Dot , Docx , Dotx , Docm , Odt , Ott.

```csharp
public static void RemoveAllSignatures(Stream srcStream, Stream dstStream)
```

## Esempi

Mostra come rimuovere le firme digitali da un documento firmato digitalmente.

```csharp
// Esistono due modi per utilizzare la classe DigitalSignatureUtil per rimuovere le firme digitali
// da un documento firmato salvandone una copia non firmata da qualche altra parte nel file system locale.
// 1 - Determina le posizioni sia del documento firmato che della copia non firmata in base alle stringhe del nome file:
DigitalSignatureUtil.RemoveAllSignatures(MyDir + "Digitally signed.docx",
    ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx");

// 2 - Determina le posizioni sia del documento firmato che della copia non firmata tramite flussi di file:
using (Stream streamIn = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx", FileMode.Create))
    {
        DigitalSignatureUtil.RemoveAllSignatures(streamIn, streamOut);
    }
}

// Verifica che entrambi i nostri documenti di output non abbiano firme digitali.
Assert.That(DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx"), Is.Empty);
Assert.That(DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx"), Is.Empty);
```

### Guarda anche

* class [DigitalSignatureUtil](../)
* spazio dei nomi [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* assemblea [Aspose.Words](../../../)
