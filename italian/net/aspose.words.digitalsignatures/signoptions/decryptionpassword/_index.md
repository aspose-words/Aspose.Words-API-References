---
title: SignOptions.DecryptionPassword
linktitle: DecryptionPassword
articleTitle: DecryptionPassword
second_title: Aspose.Words per .NET
description: Sblocca i tuoi documenti senza sforzo con la funzione DecryptionPassword di SignOptions. Decrittografa in modo sicuro i file sorgente con facilità; il valore predefinito è una stringa vuota.
type: docs
weight: 30
url: /it/net/aspose.words.digitalsignatures/signoptions/decryptionpassword/
---
## SignOptions.DecryptionPassword property

La password per decifrare il documento sorgente. Il valore predefinito è**stringa vuota** (Empty ).

```csharp
public string DecryptionPassword { get; set; }
```

## Osservazioni

Se il documento OOXML è crittografato, è necessario fornire la password di decrittazione per decrittografare il documento sorgente prima che venga firmato. Questa operazione non è richiesta per i documenti in formato binario DOC.

## Esempi

Mostra come firmare un file di documento crittografato.

```csharp
// Creare un certificato X.509 da un archivio PKCS#12, che dovrebbe contenere una chiave privata.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Crea un commento, una data e una password di decrittazione che verranno applicati con la nostra nuova firma digitale.
SignOptions signOptions = new SignOptions
{
    Comments = "Comment",
    SignTime = DateTime.Now,
    DecryptionPassword = "docPassword"
};

// Imposta un nome file di sistema locale per il documento di input non firmato e un nome file di output per la sua nuova copia firmata digitalmente.
string inputFileName = MyDir + "Encrypted.docx";
string outputFileName = ArtifactsDir + "DigitalSignatureUtil.DecryptionPassword.docx";

DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

### Guarda anche

* class [SignOptions](../)
* spazio dei nomi [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* assemblea [Aspose.Words](../../../)
