---
title: DigitalSignatureUtil
second_title: Aspose.Words per .NET API Reference
description: Fornisce i metodi per la firma del documento.
type: docs
weight: 400
url: /it/net/aspose.words.digitalsignatures/digitalsignatureutil/
---
## DigitalSignatureUtil class

Fornisce i metodi per la firma del documento.

```csharp
public static class DigitalSignatureUtil
```

## Metodi

| Nome | Descrizione |
| --- | --- |
| static [LoadSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures#loadsignatures)(Stream) | Carica le firme digitali dal documento utilizzando stream. |
| static [LoadSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures#loadsignatures_1)(string) | Carica le firme digitali dal documento. |
| static [RemoveAllSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures#removeallsignatures)(Stream, Stream) | Rimuove tutte le firme digitali dal documento nel flusso di origine e scrive il documento non firmato nel flusso di destinazione. |
| static [RemoveAllSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures#removeallsignatures_1)(string, string) | Rimuove tutte le firme digitali dal file di origine e scrive il file non firmato nel file di destinazione. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign#sign)(Stream, Stream, CertificateHolder) | Firma il documento sorgente usando dato[`CertificateHolder`](../certificateholder)con firma digitale e scrive il documento firmato nel flusso di destinazione. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign#sign_2)(string, string, CertificateHolder) | Firma il documento sorgente usando dato[`CertificateHolder`](../certificateholder) con firma digitale e scrive il documento firmato nel file di destinazione. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign#sign_1)(Stream, Stream, CertificateHolder, SignOptions) | Firma il documento sorgente usando dato[`CertificateHolder`](../certificateholder) e[`SignOptions`](../signoptions) con firma digitale e scrive il documento firmato nel flusso di destinazione. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign#sign_3)(string, string, CertificateHolder, SignOptions) | Firma il documento sorgente usando dato[`CertificateHolder`](../certificateholder) e[`SignOptions`](../signoptions) con firma digitale e scrive il documento firmato nel file di destinazione. |

### Osservazioni

Poiché la firma digitale funziona con il contenuto del file anziché con Document Object Model, questi metodi vengono inseriti in una classe separata.

I formati supportati sonoDoc eDocx.

### Esempi

Mostra come caricare le firme da un documento firmato digitalmente.

```csharp
// Esistono due modi per caricare la raccolta di firme digitali di un documento firmato utilizzando la classe DigitalSignatureUtil.
// 1 - Carica da un documento da un file system locale nome file:
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
// da un documento firmato salvandone una copia non firmata da qualche altra parte nel file system locale.
// 1 - Determina le posizioni sia del documento firmato che della copia non firmata in base alle stringhe del nome del file:
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

* spazio dei nomi [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
