---
title: CertificateHolder.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words per .NET
description: Crea senza sforzo un oggetto CertificateHolder da un array di byte PKCS12 e una password. Semplifica la gestione dei certificati con il nostro metodo intuitivo.
type: docs
weight: 10
url: /it/net/aspose.words.digitalsignatures/certificateholder/create/
---
## Create(*byte[], SecureString*) {#create}

Crea[`CertificateHolder`](../) oggetto che utilizza l'array di byte dell'archivio PKCS12 e la sua password.

```csharp
public static CertificateHolder Create(byte[] certBytes, SecureString password)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| certBytes | Byte[] | Un array di byte che contiene dati da un certificato X.509. |
| password | SecureString | Password richiesta per accedere ai dati del certificato X.509. |

### Valore di ritorno

Un esempio di[`CertificateHolder`](../)

### Eccezioni

| eccezione | condizione |
| --- | --- |
| InvalidParameterException | Lanciato se*certBytes* È`null` |
| InvalidParameterException | Lanciato se*password* È`null` |
| SecurityException | Generato se l'archivio PKCS12 non contiene alias |
| IOException | Viene generato se la password è errata o il file è danneggiato. |

## Esempi

Mostra come creare oggetti CertificateHolder.

```csharp
// Di seguito sono riportati quattro modi per creare oggetti CertificateHolder.
// 1 - Carica un file PKCS #12 in un array di byte e applica la sua password:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - Carica un file PKCS #12 in un array di byte e applica una password sicura:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Se il certificato ha chiavi private corrispondenti agli alias,
// possiamo usare gli alias per recuperare le rispettive chiavi. Per prima cosa, verificheremo la validità degli alias.
using (FileStream certStream = new FileStream(MyDir + "morzal.pfx", FileMode.Open))
{
    Pkcs12Store pkcs12Store = new Pkcs12StoreBuilder().Build();
    pkcs12Store.Load(certStream, "aw".ToCharArray());
    foreach (string currentAlias in pkcs12Store.Aliases)
    {
        if ((currentAlias != null) &&
            (pkcs12Store.IsKeyEntry(currentAlias) &&
             pkcs12Store.GetKey(currentAlias).Key.IsPrivate))
        {
            Console.WriteLine($"Valid alias found: {currentAlias}");
        }
    }
}

// 3 - Utilizzare un alias valido:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - Passare "null" come alias per utilizzare il primo alias disponibile che restituisce una chiave privata:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Guarda anche

* class [CertificateHolder](../)
* spazio dei nomi [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* assemblea [Aspose.Words](../../../)

---

## Create(*byte[], string*) {#create_1}

Crea[`CertificateHolder`](../) oggetto che utilizza l'array di byte dell'archivio PKCS12 e la sua password.

```csharp
public static CertificateHolder Create(byte[] certBytes, string password)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| certBytes | Byte[] | Un array di byte che contiene dati da un certificato X.509. |
| password | String | Password richiesta per accedere ai dati del certificato X.509. |

### Valore di ritorno

Un esempio di[`CertificateHolder`](../)

### Eccezioni

| eccezione | condizione |
| --- | --- |
| InvalidParameterException | Lanciato se*certBytes* È`null` |
| InvalidParameterException | Lanciato se*password* È`null` |
| SecurityException | Generato se l'archivio PKCS12 non contiene alias |
| IOException | Viene generato se la password è errata o il file è danneggiato. |

## Esempi

Mostra come creare oggetti CertificateHolder.

```csharp
// Di seguito sono riportati quattro modi per creare oggetti CertificateHolder.
// 1 - Carica un file PKCS #12 in un array di byte e applica la sua password:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - Carica un file PKCS #12 in un array di byte e applica una password sicura:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Se il certificato ha chiavi private corrispondenti agli alias,
// possiamo usare gli alias per recuperare le rispettive chiavi. Per prima cosa, verificheremo la validità degli alias.
using (FileStream certStream = new FileStream(MyDir + "morzal.pfx", FileMode.Open))
{
    Pkcs12Store pkcs12Store = new Pkcs12StoreBuilder().Build();
    pkcs12Store.Load(certStream, "aw".ToCharArray());
    foreach (string currentAlias in pkcs12Store.Aliases)
    {
        if ((currentAlias != null) &&
            (pkcs12Store.IsKeyEntry(currentAlias) &&
             pkcs12Store.GetKey(currentAlias).Key.IsPrivate))
        {
            Console.WriteLine($"Valid alias found: {currentAlias}");
        }
    }
}

// 3 - Utilizzare un alias valido:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - Passare "null" come alias per utilizzare il primo alias disponibile che restituisce una chiave privata:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Guarda anche

* class [CertificateHolder](../)
* spazio dei nomi [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* assemblea [Aspose.Words](../../../)

---

## Create(*string, string*) {#create_2}

Crea[`CertificateHolder`](../)oggetto che utilizza il percorso per l'archivio PKCS12 e la sua password.

```csharp
public static CertificateHolder Create(string fileName, string password)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fileName | String | Il nome di un file di certificato. |
| password | String | Password richiesta per accedere ai dati del certificato X.509. |

### Valore di ritorno

Un esempio di[`CertificateHolder`](../)

### Eccezioni

| eccezione | condizione |
| --- | --- |
| InvalidParameterException | Lanciato se*fileName* È`null` |
| InvalidParameterException | Lanciato se*password* È`null` |
| SecurityException | Generato se l'archivio PKCS12 non contiene alias |
| IOException | Viene generato se la password è errata o il file è danneggiato. |

## Esempi

Mostra come firmare digitalmente i documenti.

```csharp
// Creare un certificato X.509 da un archivio PKCS#12, che dovrebbe contenere una chiave privata.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Crea un commento e una data che verranno applicati con la nostra nuova firma digitale.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// Prendi un documento non firmato dal file system locale tramite un flusso di file,
// quindi crea una copia firmata determinata dal nome file del flusso di file di output.
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

### Guarda anche

* class [CertificateHolder](../)
* spazio dei nomi [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* assemblea [Aspose.Words](../../../)

---

## Create(*string, string, string*) {#create_3}

Crea[`CertificateHolder`](../) oggetto che utilizza il percorso per l'archivio PKCS12, la sua password e l'alias utilizzando quale chiave privata e certificato verranno trovati.

```csharp
public static CertificateHolder Create(string fileName, string password, string alias)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fileName | String | Il nome di un file di certificato. |
| password | String | Password richiesta per accedere ai dati del certificato X.509. |
| alias | String | L'alias associato per un certificato e la sua chiave privata |

### Valore di ritorno

Un esempio di[`CertificateHolder`](../)

### Eccezioni

| eccezione | condizione |
| --- | --- |
| InvalidParameterException | Lanciato se*fileName* È`null` |
| InvalidParameterException | Lanciato se*password* È`null` |
| SecurityException | Generato se l'archivio PKCS12 non contiene alias |
| IOException | Viene generato se la password è errata o il file è danneggiato. |
| SecurityException | Generato se non esiste una chiave privata con l'alias specificato |

## Esempi

Mostra come creare oggetti CertificateHolder.

```csharp
// Di seguito sono riportati quattro modi per creare oggetti CertificateHolder.
// 1 - Carica un file PKCS #12 in un array di byte e applica la sua password:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - Carica un file PKCS #12 in un array di byte e applica una password sicura:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Se il certificato ha chiavi private corrispondenti agli alias,
// possiamo usare gli alias per recuperare le rispettive chiavi. Per prima cosa, verificheremo la validità degli alias.
using (FileStream certStream = new FileStream(MyDir + "morzal.pfx", FileMode.Open))
{
    Pkcs12Store pkcs12Store = new Pkcs12StoreBuilder().Build();
    pkcs12Store.Load(certStream, "aw".ToCharArray());
    foreach (string currentAlias in pkcs12Store.Aliases)
    {
        if ((currentAlias != null) &&
            (pkcs12Store.IsKeyEntry(currentAlias) &&
             pkcs12Store.GetKey(currentAlias).Key.IsPrivate))
        {
            Console.WriteLine($"Valid alias found: {currentAlias}");
        }
    }
}

// 3 - Utilizzare un alias valido:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - Passare "null" come alias per utilizzare il primo alias disponibile che restituisce una chiave privata:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Guarda anche

* class [CertificateHolder](../)
* spazio dei nomi [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* assemblea [Aspose.Words](../../../)
