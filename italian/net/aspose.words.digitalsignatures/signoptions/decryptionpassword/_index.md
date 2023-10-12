---
title: SignOptions.DecryptionPassword
second_title: Aspose.Words per .NET API Reference
description: SignOptions proprietà. La password per decrittografare il documento di origine. Il valore predefinito è stringa vuota Empty.
type: docs
weight: 30
url: /it/net/aspose.words.digitalsignatures/signoptions/decryptionpassword/
---
## SignOptions.DecryptionPassword property

La password per decrittografare il documento di origine. Il valore predefinito è **stringa vuota** (Empty).

```csharp
public string DecryptionPassword { get; set; }
```

### Osservazioni

Se il documento OOXML è crittografato, è necessario fornire la password di decrittografia per decrittografare il documento di origine prima che venga firmato. Questa non è richiesta per i documenti in formato DOC binario.

### Esempi

Mostra come firmare un file di documento crittografato.

```csharp
// Crea un certificato X.509 da un archivio PKCS#12, che dovrebbe contenere una chiave privata.
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
* spazio dei nomi [Aspose.Words.DigitalSignatures](../../signoptions/)
* assemblea [Aspose.Words](../../../)


