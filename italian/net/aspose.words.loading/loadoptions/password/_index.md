---
title: LoadOptions.Password
linktitle: Password
articleTitle: Password
second_title: Aspose.Words per .NET
description: Gestisci i tuoi documenti crittografati senza sforzo con la proprietà Password di LoadOptions. Imposta o recupera la tua password in modo sicuro per un accesso senza interruzioni.
type: docs
weight: 110
url: /it/net/aspose.words.loading/loadoptions/password/
---
## LoadOptions.Password property

Ottiene o imposta la password per l'apertura di un documento crittografato. Può essere`null` o stringa vuota. Il valore predefinito è`null` .

```csharp
public string Password { get; set; }
```

## Osservazioni

È necessario conoscere la password per aprire un documento crittografato. Se il documento non è crittografato, impostarla su`null` o stringa vuota.

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

* class [LoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../../aspose.words.loading/)
* assemblea [Aspose.Words](../../../)
