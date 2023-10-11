---
title: CertificateHolder.Create
second_title: Aspose.Words per .NET API Reference
description: CertificateHolder metodo. CreaCertificateHolder oggetto che utilizza larray di byte dellarchivio PKCS12 e la relativa password.
type: docs
weight: 10
url: /it/net/aspose.words.digitalsignatures/certificateholder/create/
---
## Create(byte[], SecureString) {#create}

Crea[`CertificateHolder`](../) oggetto che utilizza l'array di byte dell'archivio PKCS12 e la relativa password.

```csharp
public static CertificateHolder Create(byte[] certBytes, SecureString password)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| certBytes | Byte[] | Una matrice di byte che contiene i dati di un certificato X.509. |
| password | SecureString | La password richiesta per accedere ai dati del certificato X.509. |

### Valore di ritorno

Un'istanza di[`CertificateHolder`](../)

### Eccezioni

| eccezione | condizione |
| --- | --- |
| InvalidParameterException | Gettato se*certBytes* È`nullo` |
| InvalidParameterException | Gettato se*password* È`nullo` |
| SecurityException | Emesso se l'archivio PKCS12 non contiene alias |
| IOException | Emesso se è presente una password errata o un file danneggiato. |

### Esempi

Mostra come creare oggetti CertificateHolder.

```csharp
// Di seguito sono riportati quattro modi per creare oggetti CertificateHolder.
// 1 - Carica un file PKCS #12 in un array di byte e applica la sua password:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - Carica un file PKCS #12 in un array di byte e applica una password sicura:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Se il certificato ha chiavi private corrispondenti ad alias,
// possiamo usare gli alias per recuperare le rispettive chiavi. Innanzitutto, controlleremo gli alias validi.
using (FileStream certStream = new FileStream(MyDir + "morzal.pfx", FileMode.Open))
{
    Pkcs12Store pkcs12Store = new Pkcs12StoreBuilder().Build();
    pkcs12Store.Load(certStream, "aw".ToCharArray());
    IEnumerator enumerator = pkcs12Store.Aliases.GetEnumerator();

    while (enumerator.MoveNext())
    {
        if (enumerator.Current != null)
        {
            string currentAlias = enumerator.Current.ToString();
            if (pkcs12Store.IsKeyEntry(currentAlias) && pkcs12Store.GetKey(currentAlias).Key.IsPrivate)
            {
                Console.WriteLine($"Valid alias found: {enumerator.Current}");
            }
        }
    }
}

// 3 - Utilizza un alias valido:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - Passa "null" come alias per utilizzare il primo alias disponibile che restituisce una chiave privata:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Guarda anche

* class [CertificateHolder](../)
* spazio dei nomi [Aspose.Words.DigitalSignatures](../../certificateholder/)
* assemblea [Aspose.Words](../../../)

---

## Create(byte[], string) {#create_1}

Crea[`CertificateHolder`](../) oggetto che utilizza l'array di byte dell'archivio PKCS12 e la relativa password.

```csharp
public static CertificateHolder Create(byte[] certBytes, string password)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| certBytes | Byte[] | Una matrice di byte che contiene i dati di un certificato X.509. |
| password | String | La password richiesta per accedere ai dati del certificato X.509. |

### Valore di ritorno

Un'istanza di[`CertificateHolder`](../)

### Eccezioni

| eccezione | condizione |
| --- | --- |
| InvalidParameterException | Gettato se*certBytes* È`nullo` |
| InvalidParameterException | Gettato se*password* È`nullo` |
| SecurityException | Emesso se l'archivio PKCS12 non contiene alias |
| IOException | Emesso se è presente una password errata o un file danneggiato. |

### Esempi

Mostra come creare oggetti CertificateHolder.

```csharp
// Di seguito sono riportati quattro modi per creare oggetti CertificateHolder.
// 1 - Carica un file PKCS #12 in un array di byte e applica la sua password:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - Carica un file PKCS #12 in un array di byte e applica una password sicura:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Se il certificato ha chiavi private corrispondenti ad alias,
// possiamo usare gli alias per recuperare le rispettive chiavi. Innanzitutto, controlleremo gli alias validi.
using (FileStream certStream = new FileStream(MyDir + "morzal.pfx", FileMode.Open))
{
    Pkcs12Store pkcs12Store = new Pkcs12StoreBuilder().Build();
    pkcs12Store.Load(certStream, "aw".ToCharArray());
    IEnumerator enumerator = pkcs12Store.Aliases.GetEnumerator();

    while (enumerator.MoveNext())
    {
        if (enumerator.Current != null)
        {
            string currentAlias = enumerator.Current.ToString();
            if (pkcs12Store.IsKeyEntry(currentAlias) && pkcs12Store.GetKey(currentAlias).Key.IsPrivate)
            {
                Console.WriteLine($"Valid alias found: {enumerator.Current}");
            }
        }
    }
}

// 3 - Utilizza un alias valido:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - Passa "null" come alias per utilizzare il primo alias disponibile che restituisce una chiave privata:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Guarda anche

* class [CertificateHolder](../)
* spazio dei nomi [Aspose.Words.DigitalSignatures](../../certificateholder/)
* assemblea [Aspose.Words](../../../)

---

## Create(string, string) {#create_2}

Crea[`CertificateHolder`](../) oggetto utilizzando il percorso dell'archivio PKCS12 e la relativa password.

```csharp
public static CertificateHolder Create(string fileName, string password)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fileName | String | Il nome di un file di certificato. |
| password | String | La password richiesta per accedere ai dati del certificato X.509. |

### Valore di ritorno

Un'istanza di[`CertificateHolder`](../)

### Eccezioni

| eccezione | condizione |
| --- | --- |
| InvalidParameterException | Gettato se*fileName* È`nullo` |
| InvalidParameterException | Gettato se*password* È`nullo` |
| SecurityException | Emesso se l'archivio PKCS12 non contiene alias |
| IOException | Emesso se è presente una password errata o un file danneggiato. |

### Esempi

Mostra come firmare digitalmente i documenti.

```csharp
// Crea un certificato X.509 da un archivio PKCS#12, che dovrebbe contenere una chiave privata.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Crea un commento e una data che verranno applicati con la nostra nuova firma digitale.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// Preleva un documento non firmato dal file system locale tramite un flusso di file,
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
* spazio dei nomi [Aspose.Words.DigitalSignatures](../../certificateholder/)
* assemblea [Aspose.Words](../../../)

---

## Create(string, string, string) {#create_3}

Crea[`CertificateHolder`](../) oggetto utilizzando il percorso dell'archivio PKCS12, la relativa password e l'alias utilizzando la chiave privata e il certificato che verranno trovati.

```csharp
public static CertificateHolder Create(string fileName, string password, string alias)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fileName | String | Il nome di un file di certificato. |
| password | String | La password richiesta per accedere ai dati del certificato X.509. |
| alias | String | L'alias associato a un certificato e alla relativa chiave privata |

### Valore di ritorno

Un'istanza di[`CertificateHolder`](../)

### Eccezioni

| eccezione | condizione |
| --- | --- |
| InvalidParameterException | Gettato se*fileName* È`nullo` |
| InvalidParameterException | Gettato se*password* È`nullo` |
| SecurityException | Emesso se l'archivio PKCS12 non contiene alias |
| IOException | Emesso se è presente una password errata o un file danneggiato. |
| SecurityException | Emesso se non è presente una chiave privata con l'alias specificato |

### Esempi

Mostra come creare oggetti CertificateHolder.

```csharp
// Di seguito sono riportati quattro modi per creare oggetti CertificateHolder.
// 1 - Carica un file PKCS #12 in un array di byte e applica la sua password:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - Carica un file PKCS #12 in un array di byte e applica una password sicura:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Se il certificato ha chiavi private corrispondenti ad alias,
// possiamo usare gli alias per recuperare le rispettive chiavi. Innanzitutto, controlleremo gli alias validi.
using (FileStream certStream = new FileStream(MyDir + "morzal.pfx", FileMode.Open))
{
    Pkcs12Store pkcs12Store = new Pkcs12StoreBuilder().Build();
    pkcs12Store.Load(certStream, "aw".ToCharArray());
    IEnumerator enumerator = pkcs12Store.Aliases.GetEnumerator();

    while (enumerator.MoveNext())
    {
        if (enumerator.Current != null)
        {
            string currentAlias = enumerator.Current.ToString();
            if (pkcs12Store.IsKeyEntry(currentAlias) && pkcs12Store.GetKey(currentAlias).Key.IsPrivate)
            {
                Console.WriteLine($"Valid alias found: {enumerator.Current}");
            }
        }
    }
}

// 3 - Utilizza un alias valido:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - Passa "null" come alias per utilizzare il primo alias disponibile che restituisce una chiave privata:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Guarda anche

* class [CertificateHolder](../)
* spazio dei nomi [Aspose.Words.DigitalSignatures](../../certificateholder/)
* assemblea [Aspose.Words](../../../)


