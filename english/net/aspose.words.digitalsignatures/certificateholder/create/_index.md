---
title: Create
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 10
url: /net/aspose.words.digitalsignatures/certificateholder/create/
---
## Create(byte[], SecureString) {#create}

Creates CertificateHolder object using byte array of PKCS12 store and its password.

```csharp
public static CertificateHolder Create(byte[] certBytes, SecureString password)
```

| Parameter | Type | Description |
| --- | --- | --- |
| certBytes | Byte[] | A byte array that contains data from an X.509 certificate. |
| password | SecureString | The password required to access the X.509 certificate data. |

### Return Value

An instance of CertificateHolder

### Exceptions

| exception | condition |
| --- | --- |
| InvalidParameterException | Thrown if **certBytes** is null |
| InvalidParameterException | Thrown if **password** is null |
| SecurityException | Thrown if PKCS12 store contains no aliases |
| IOException | Thrown if there is wrong password or corrupted file. |

### Examples

Shows how to create CertificateHolder objects.

```csharp
// Below are four ways of creating CertificateHolder objects.
// 1 -  Load a PKCS #12 file into a byte array and apply its password:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 -  Load a PKCS #12 file into a byte array, and apply a secure password:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// If the certificate has private keys corresponding to aliases,
// we can use the aliases to fetch their respective keys. First, we will check for valid aliases.
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

// 3 -  Use a valid alias:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 -  Pass "null" as the alias in order to use the first available alias that returns a private key:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### See Also

* class [CertificateHolder](../../certificateholder)
* namespace [Aspose.Words.DigitalSignatures](../../certificateholder)
* assembly [Aspose.Words](../../../)

---

## Create(byte[], string) {#create_1}

Creates CertificateHolder object using byte array of PKCS12 store and its password.

```csharp
public static CertificateHolder Create(byte[] certBytes, string password)
```

| Parameter | Type | Description |
| --- | --- | --- |
| certBytes | Byte[] | A byte array that contains data from an X.509 certificate. |
| password | String | The password required to access the X.509 certificate data. |

### Return Value

An instance of CertificateHolder

### Exceptions

| exception | condition |
| --- | --- |
| InvalidParameterException | Thrown if **certBytes** is null |
| InvalidParameterException | Thrown if **password** is null |
| SecurityException | Thrown if PKCS12 store contains no aliases |
| IOException | Thrown if there is wrong password or corrupted file. |

### Examples

Shows how to create CertificateHolder objects.

```csharp
// Below are four ways of creating CertificateHolder objects.
// 1 -  Load a PKCS #12 file into a byte array and apply its password:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 -  Load a PKCS #12 file into a byte array, and apply a secure password:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// If the certificate has private keys corresponding to aliases,
// we can use the aliases to fetch their respective keys. First, we will check for valid aliases.
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

// 3 -  Use a valid alias:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 -  Pass "null" as the alias in order to use the first available alias that returns a private key:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### See Also

* class [CertificateHolder](../../certificateholder)
* namespace [Aspose.Words.DigitalSignatures](../../certificateholder)
* assembly [Aspose.Words](../../../)

---

## Create(string, string) {#create_2}

Creates CertificateHolder object using path to PKCS12 store and its password.

```csharp
public static CertificateHolder Create(string fileName, string password)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | String | The name of a certificate file. |
| password | String | The password required to access the X.509 certificate data. |

### Return Value

An instance of CertificateHolder

### Exceptions

| exception | condition |
| --- | --- |
| InvalidParameterException | Thrown if **fileName** is null |
| InvalidParameterException | Thrown if **password** is null |
| SecurityException | Thrown if PKCS12 store contains no aliases |
| IOException | Thrown if there is wrong password or corrupted file. |

### Examples

Shows how to digitally sign documents.

```csharp
// Create an X.509 certificate from a PKCS#12 store, which should contain a private key.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Create a comment and date which will be applied with our new digital signature.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// Take an unsigned document from the local file system via a file stream,
// then create a signed copy of it determined by the filename of the output file stream.
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

### See Also

* class [CertificateHolder](../../certificateholder)
* namespace [Aspose.Words.DigitalSignatures](../../certificateholder)
* assembly [Aspose.Words](../../../)

---

## Create(string, string, string) {#create_3}

Creates CertificateHolder object using path to PKCS12 store, its password and the alias by using which private key and certificate will be found.

```csharp
public static CertificateHolder Create(string fileName, string password, string alias)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | String | The name of a certificate file. |
| password | String | The password required to access the X.509 certificate data. |
| alias | String | The associated alias for a certificate and its private key |

### Return Value

An instance of CertificateHolder

### Exceptions

| exception | condition |
| --- | --- |
| InvalidParameterException | Thrown if **fileName** is null |
| InvalidParameterException | Thrown if **password** is null |
| SecurityException | Thrown if PKCS12 store contains no aliases |
| IOException | Thrown if there is wrong password or corrupted file. |
| SecurityException | Thrown if there is no private key with the given alias |

### Examples

Shows how to create CertificateHolder objects.

```csharp
// Below are four ways of creating CertificateHolder objects.
// 1 -  Load a PKCS #12 file into a byte array and apply its password:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 -  Load a PKCS #12 file into a byte array, and apply a secure password:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// If the certificate has private keys corresponding to aliases,
// we can use the aliases to fetch their respective keys. First, we will check for valid aliases.
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

// 3 -  Use a valid alias:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 -  Pass "null" as the alias in order to use the first available alias that returns a private key:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### See Also

* class [CertificateHolder](../../certificateholder)
* namespace [Aspose.Words.DigitalSignatures](../../certificateholder)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
