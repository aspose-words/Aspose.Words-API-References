---
title: LoadOptions.Password
second_title: Aspose.Words per .NET API Reference
description: LoadOptions proprietà. Ottiene o imposta la password per lapertura di un documento crittografato. Può esserenullo o stringa vuota. Limpostazione predefinita ènullo .
type: docs
weight: 110
url: /it/net/aspose.words.loading/loadoptions/password/
---
## LoadOptions.Password property

Ottiene o imposta la password per l'apertura di un documento crittografato. Può essere`nullo` o stringa vuota. L'impostazione predefinita è`nullo` .

```csharp
public string Password { get; set; }
```

### Osservazioni

È necessario conoscere la password per aprire un documento crittografato. Se il documento non è crittografato, impostalo su`nullo` o stringa vuota.

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

* class [LoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../loadoptions/)
* assemblea [Aspose.Words](../../../)


