---
title: Create
second_title: Aspose.Words per .NET API Reference
description: Crea oggetto CertificateHolder utilizzando larray di byte dellarchivio PKCS12 e la relativa password.
type: docs
weight: 10
url: /it/net/aspose.words.digitalsignatures/certificateholder/create/
---
## Create(byte[], SecureString) {#create}

Crea oggetto CertificateHolder utilizzando l'array di byte dell'archivio PKCS12 e la relativa password.

```csharp
public static CertificateHolder Create(byte[] certBytes, SecureString password)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| certBytes | Byte[] | Matrice di byte che contiene dati da un certificato X.509. |
| password | SecureString | La password richiesta per accedere ai dati del certificato X.509. |

### Valore di ritorno

Un'istanza di CertificateHolder

### Eccezioni

| eccezione | condizione |
| --- | --- |
| InvalidParameterException | Lanciato se **certBytes** è zero |
| InvalidParameterException | Lanciato se **parola d'ordine** è zero |
| SecurityException | Generato se il negozio PKCS12 non contiene alias |
| IOException | Generato se è presente una password errata o un file danneggiato. |

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

// Se il certificato ha chiavi private corrispondenti agli alias,
// possiamo usare gli alias per recuperare le rispettive chiavi. Innanzitutto, verificheremo la presenza di alias validi.
using (FileStream certStream = new FileStream(MyDir + "morzal.pfx", FileMode.Open))
{
    Pkcs12Store pkcs12Store = new Pkcs12Store(certStream, "aw".ToCharArray());
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

// 3 - Usa un alias valido:
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

Crea oggetto CertificateHolder utilizzando l'array di byte dell'archivio PKCS12 e la relativa password.

```csharp
public static CertificateHolder Create(byte[] certBytes, string password)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| certBytes | Byte[] | Matrice di byte che contiene dati da un certificato X.509. |
| password | String | La password richiesta per accedere ai dati del certificato X.509. |

### Valore di ritorno

Un'istanza di CertificateHolder

### Eccezioni

| eccezione | condizione |
| --- | --- |
| InvalidParameterException | Lanciato se **certBytes** è zero |
| InvalidParameterException | Lanciato se **parola d'ordine** è zero |
| SecurityException | Generato se il negozio PKCS12 non contiene alias |
| IOException | Generato se è presente una password errata o un file danneggiato. |

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

// Se il certificato ha chiavi private corrispondenti agli alias,
// possiamo usare gli alias per recuperare le rispettive chiavi. Innanzitutto, verificheremo la presenza di alias validi.
using (FileStream certStream = new FileStream(MyDir + "morzal.pfx", FileMode.Open))
{
    Pkcs12Store pkcs12Store = new Pkcs12Store(certStream, "aw".ToCharArray());
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

// 3 - Usa un alias valido:
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

Crea oggetto CertificateHolder utilizzando il percorso dell'archivio PKCS12 e la relativa password.

```csharp
public static CertificateHolder Create(string fileName, string password)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fileName | String | Il nome di un file di certificato. |
| password | String | La password richiesta per accedere ai dati del certificato X.509. |

### Valore di ritorno

Un'istanza di CertificateHolder

### Eccezioni

| eccezione | condizione |
| --- | --- |
| InvalidParameterException | Lanciato se **nome del file** è zero |
| InvalidParameterException | Lanciato se **parola d'ordine** è zero |
| SecurityException | Generato se il negozio PKCS12 non contiene alias |
| IOException | Generato se è presente una password errata o un file danneggiato. |

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

// Prendi un documento non firmato dal file system locale tramite un flusso di file,
// quindi creane una copia firmata determinata dal nome del file del flusso di file di output.
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

Crea l'oggetto CertificateHolder utilizzando il percorso dell'archivio PKCS12, la relativa password e l'alias utilizzando quale chiave privata e certificato verranno trovati.

```csharp
public static CertificateHolder Create(string fileName, string password, string alias)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fileName | String | Il nome di un file di certificato. |
| password | String | La password richiesta per accedere ai dati del certificato X.509. |
| alias | String | L'alias associato per un certificato e la relativa chiave privata |

### Valore di ritorno

Un'istanza di CertificateHolder

### Eccezioni

| eccezione | condizione |
| --- | --- |
| InvalidParameterException | Lanciato se **nome del file** è zero |
| InvalidParameterException | Lanciato se **parola d'ordine** è zero |
| SecurityException | Generato se il negozio PKCS12 non contiene alias |
| IOException | Generato se è presente una password errata o un file danneggiato. |
| SecurityException | Generato se non esiste una chiave privata con l'alias specificato |

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

// Se il certificato ha chiavi private corrispondenti agli alias,
// possiamo usare gli alias per recuperare le rispettive chiavi. Innanzitutto, verificheremo la presenza di alias validi.
using (FileStream certStream = new FileStream(MyDir + "morzal.pfx", FileMode.Open))
{
    Pkcs12Store pkcs12Store = new Pkcs12Store(certStream, "aw".ToCharArray());
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

// 3 - Usa un alias valido:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - Passa "null" come alias per utilizzare il primo alias disponibile che restituisce una chiave privata:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Guarda anche

* class [CertificateHolder](../)
* spazio dei nomi [Aspose.Words.DigitalSignatures](../../certificateholder/)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
