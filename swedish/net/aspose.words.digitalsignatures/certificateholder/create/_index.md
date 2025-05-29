---
title: CertificateHolder.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words för .NET
description: Skapa enkelt ett CertificateHolder-objekt från en PKCS12-byte-array och lösenord. Förenkla certifikathanteringen med vår intuitiva metod.
type: docs
weight: 10
url: /sv/net/aspose.words.digitalsignatures/certificateholder/create/
---
## Create(*byte[], SecureString*) {#create}

Skapar[`CertificateHolder`](../) objekt som använder byte-arrayen för PKCS12-arkivet och dess lösenord.

```csharp
public static CertificateHolder Create(byte[] certBytes, SecureString password)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| certBytes | Byte[] | En byte-array som innehåller data från ett X.509-certifikat. |
| password | SecureString | Lösenordet som krävs för att komma åt X.509-certifikatdata. |

### Returvärde

Ett exempel på[`CertificateHolder`](../)

### Undantag

| undantag | skick |
| --- | --- |
| InvalidParameterException | Kastad om*certBytes* är`null` |
| InvalidParameterException | Kastad om*password* är`null` |
| SecurityException | Utlöses om PKCS12-arkivet inte innehåller några alias |
| IOException | Körs om det finns fel lösenord eller en skadad fil. |

## Exempel

Visar hur man skapar CertificateHolder-objekt.

```csharp
// Nedan följer fyra sätt att skapa CertificateHolder-objekt.
// 1 - Ladda in en PKCS #12-fil i en byte-array och använd dess lösenord:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - Ladda in en PKCS #12-fil i en byte-array och använd ett säkert lösenord:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Om certifikatet har privata nycklar som motsvarar alias,
// vi kan använda aliasen för att hämta deras respektive nycklar. Först kontrollerar vi om det finns giltiga alias.
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

// 3 - Använd ett giltigt alias:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - Skicka "null" som alias för att använda det första tillgängliga aliaset som returnerar en privat nyckel:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Se även

* class [CertificateHolder](../)
* namnutrymme [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* hopsättning [Aspose.Words](../../../)

---

## Create(*byte[], string*) {#create_1}

Skapar[`CertificateHolder`](../) objekt som använder byte-arrayen för PKCS12-arkivet och dess lösenord.

```csharp
public static CertificateHolder Create(byte[] certBytes, string password)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| certBytes | Byte[] | En byte-array som innehåller data från ett X.509-certifikat. |
| password | String | Lösenordet som krävs för att komma åt X.509-certifikatdata. |

### Returvärde

Ett exempel på[`CertificateHolder`](../)

### Undantag

| undantag | skick |
| --- | --- |
| InvalidParameterException | Kastad om*certBytes* är`null` |
| InvalidParameterException | Kastad om*password* är`null` |
| SecurityException | Utlöses om PKCS12-arkivet inte innehåller några alias |
| IOException | Körs om det finns fel lösenord eller en skadad fil. |

## Exempel

Visar hur man skapar CertificateHolder-objekt.

```csharp
// Nedan följer fyra sätt att skapa CertificateHolder-objekt.
// 1 - Ladda in en PKCS #12-fil i en byte-array och använd dess lösenord:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - Ladda in en PKCS #12-fil i en byte-array och använd ett säkert lösenord:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Om certifikatet har privata nycklar som motsvarar alias,
// vi kan använda aliasen för att hämta deras respektive nycklar. Först kontrollerar vi om det finns giltiga alias.
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

// 3 - Använd ett giltigt alias:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - Skicka "null" som alias för att använda det första tillgängliga aliaset som returnerar en privat nyckel:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Se även

* class [CertificateHolder](../)
* namnutrymme [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* hopsättning [Aspose.Words](../../../)

---

## Create(*string, string*) {#create_2}

Skapar[`CertificateHolder`](../)objekt med sökvägen till PKCS12-arkivet och dess lösenord.

```csharp
public static CertificateHolder Create(string fileName, string password)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | String | Namnet på en certifikatfil. |
| password | String | Lösenordet som krävs för att komma åt X.509-certifikatdata. |

### Returvärde

Ett exempel på[`CertificateHolder`](../)

### Undantag

| undantag | skick |
| --- | --- |
| InvalidParameterException | Kastad om*fileName* är`null` |
| InvalidParameterException | Kastad om*password* är`null` |
| SecurityException | Utlöses om PKCS12-arkivet inte innehåller några alias |
| IOException | Körs om det finns fel lösenord eller en skadad fil. |

## Exempel

Visar hur man signerar dokument digitalt.

```csharp
// Skapa ett X.509-certifikat från ett PKCS#12-arkiv, vilket ska innehålla en privat nyckel.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Skapa en kommentar och ett datum som kommer att tillämpas med vår nya digitala signatur.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// Hämta ett osignerat dokument från det lokala filsystemet via en filström,
// skapa sedan en signerad kopia av den som bestäms av filnamnet på utdatafilströmmen.
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

### Se även

* class [CertificateHolder](../)
* namnutrymme [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* hopsättning [Aspose.Words](../../../)

---

## Create(*string, string, string*) {#create_3}

Skapar[`CertificateHolder`](../) objekt med sökvägen till PKCS12-arkivet, dess lösenord och alias med vilket privat nyckel och certifikat som ska hittas.

```csharp
public static CertificateHolder Create(string fileName, string password, string alias)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | String | Namnet på en certifikatfil. |
| password | String | Lösenordet som krävs för att komma åt X.509-certifikatdata. |
| alias | String | Det associerade aliaset för ett certifikat och dess privata nyckel |

### Returvärde

Ett exempel på[`CertificateHolder`](../)

### Undantag

| undantag | skick |
| --- | --- |
| InvalidParameterException | Kastad om*fileName* är`null` |
| InvalidParameterException | Kastad om*password* är`null` |
| SecurityException | Utlöses om PKCS12-arkivet inte innehåller några alias |
| IOException | Körs om det finns fel lösenord eller en skadad fil. |
| SecurityException | Utlöses om det inte finns någon privat nyckel med angivet aliaset |

## Exempel

Visar hur man skapar CertificateHolder-objekt.

```csharp
// Nedan följer fyra sätt att skapa CertificateHolder-objekt.
// 1 - Ladda in en PKCS #12-fil i en byte-array och använd dess lösenord:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - Ladda in en PKCS #12-fil i en byte-array och använd ett säkert lösenord:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Om certifikatet har privata nycklar som motsvarar alias,
// vi kan använda aliasen för att hämta deras respektive nycklar. Först kontrollerar vi om det finns giltiga alias.
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

// 3 - Använd ett giltigt alias:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - Skicka "null" som alias för att använda det första tillgängliga aliaset som returnerar en privat nyckel:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Se även

* class [CertificateHolder](../)
* namnutrymme [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* hopsättning [Aspose.Words](../../../)
