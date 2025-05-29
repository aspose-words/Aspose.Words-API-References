---
title: CertificateHolder.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words pour .NET
description: Créez facilement un objet CertificateHolder à partir d'un tableau d'octets PKCS12 et d'un mot de passe. Simplifiez la gestion des certificats grâce à notre méthode intuitive.
type: docs
weight: 10
url: /fr/net/aspose.words.digitalsignatures/certificateholder/create/
---
## Create(*byte[], SecureString*) {#create}

Crée[`CertificateHolder`](../) objet utilisant un tableau d'octets de stockage PKCS12 et son mot de passe.

```csharp
public static CertificateHolder Create(byte[] certBytes, SecureString password)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| certBytes | Byte[] | Un tableau d’octets contenant des données provenant d’un certificat X.509. |
| password | SecureString | Le mot de passe requis pour accéder aux données du certificat X.509. |

### Return_Value

Un exemple de[`CertificateHolder`](../)

### Exceptions

| exception | condition |
| --- | --- |
| InvalidParameterException | Jeté si*certBytes* est`nul` |
| InvalidParameterException | Jeté si*password* est`nul` |
| SecurityException | Lancé si le magasin PKCS12 ne contient aucun alias |
| IOException | Lancé s'il y a un mot de passe incorrect ou un fichier corrompu. |

## Exemples

Montre comment créer des objets CertificateHolder.

```csharp
// Vous trouverez ci-dessous quatre façons de créer des objets CertificateHolder.
// 1 - Chargez un fichier PKCS #12 dans un tableau d'octets et appliquez son mot de passe :
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - Chargez un fichier PKCS #12 dans un tableau d'octets et appliquez un mot de passe sécurisé :
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Si le certificat possède des clés privées correspondant à des alias,
// Nous pouvons utiliser les alias pour récupérer leurs clés respectives. Nous allons d'abord vérifier la validité des alias.
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

// 3 - Utiliser un alias valide :
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - Passez « null » comme alias afin d'utiliser le premier alias disponible qui renvoie une clé privée :
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Voir également

* class [CertificateHolder](../)
* espace de noms [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* Assemblée [Aspose.Words](../../../)

---

## Create(*byte[], string*) {#create_1}

Crée[`CertificateHolder`](../) objet utilisant un tableau d'octets de stockage PKCS12 et son mot de passe.

```csharp
public static CertificateHolder Create(byte[] certBytes, string password)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| certBytes | Byte[] | Un tableau d’octets contenant des données provenant d’un certificat X.509. |
| password | String | Le mot de passe requis pour accéder aux données du certificat X.509. |

### Return_Value

Un exemple de[`CertificateHolder`](../)

### Exceptions

| exception | condition |
| --- | --- |
| InvalidParameterException | Jeté si*certBytes* est`nul` |
| InvalidParameterException | Jeté si*password* est`nul` |
| SecurityException | Lancé si le magasin PKCS12 ne contient aucun alias |
| IOException | Lancé s'il y a un mot de passe incorrect ou un fichier corrompu. |

## Exemples

Montre comment créer des objets CertificateHolder.

```csharp
// Vous trouverez ci-dessous quatre façons de créer des objets CertificateHolder.
// 1 - Chargez un fichier PKCS #12 dans un tableau d'octets et appliquez son mot de passe :
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - Chargez un fichier PKCS #12 dans un tableau d'octets et appliquez un mot de passe sécurisé :
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Si le certificat possède des clés privées correspondant à des alias,
// Nous pouvons utiliser les alias pour récupérer leurs clés respectives. Nous allons d'abord vérifier la validité des alias.
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

// 3 - Utiliser un alias valide :
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - Passez « null » comme alias afin d'utiliser le premier alias disponible qui renvoie une clé privée :
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Voir également

* class [CertificateHolder](../)
* espace de noms [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* Assemblée [Aspose.Words](../../../)

---

## Create(*string, string*) {#create_2}

Crée[`CertificateHolder`](../)objet utilisant le chemin vers le magasin PKCS12 et son mot de passe.

```csharp
public static CertificateHolder Create(string fileName, string password)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fileName | String | Le nom d'un fichier de certificat. |
| password | String | Le mot de passe requis pour accéder aux données du certificat X.509. |

### Return_Value

Un exemple de[`CertificateHolder`](../)

### Exceptions

| exception | condition |
| --- | --- |
| InvalidParameterException | Jeté si*fileName* est`nul` |
| InvalidParameterException | Jeté si*password* est`nul` |
| SecurityException | Lancé si le magasin PKCS12 ne contient aucun alias |
| IOException | Lancé s'il y a un mot de passe incorrect ou un fichier corrompu. |

## Exemples

Montre comment signer numériquement des documents.

```csharp
// Créez un certificat X.509 à partir d'un magasin PKCS#12, qui doit contenir une clé privée.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Créez un commentaire et une date qui seront appliqués avec notre nouvelle signature numérique.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// Prendre un document non signé du système de fichiers local via un flux de fichiers,
// puis créez une copie signée de celui-ci déterminée par le nom de fichier du flux de fichiers de sortie.
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

### Voir également

* class [CertificateHolder](../)
* espace de noms [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* Assemblée [Aspose.Words](../../../)

---

## Create(*string, string, string*) {#create_3}

Crée[`CertificateHolder`](../) objet utilisant le chemin d'accès au magasin PKCS12, son mot de passe et l'alias à l'aide duquel la clé privée et le certificat seront trouvés.

```csharp
public static CertificateHolder Create(string fileName, string password, string alias)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fileName | String | Le nom d'un fichier de certificat. |
| password | String | Le mot de passe requis pour accéder aux données du certificat X.509. |
| alias | String | L'alias associé à un certificat et sa clé privée |

### Return_Value

Un exemple de[`CertificateHolder`](../)

### Exceptions

| exception | condition |
| --- | --- |
| InvalidParameterException | Jeté si*fileName* est`nul` |
| InvalidParameterException | Jeté si*password* est`nul` |
| SecurityException | Lancé si le magasin PKCS12 ne contient aucun alias |
| IOException | Lancé s'il y a un mot de passe incorrect ou un fichier corrompu. |
| SecurityException | Lancé s'il n'y a pas de clé privée avec l'alias donné |

## Exemples

Montre comment créer des objets CertificateHolder.

```csharp
// Vous trouverez ci-dessous quatre façons de créer des objets CertificateHolder.
// 1 - Chargez un fichier PKCS #12 dans un tableau d'octets et appliquez son mot de passe :
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - Chargez un fichier PKCS #12 dans un tableau d'octets et appliquez un mot de passe sécurisé :
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Si le certificat possède des clés privées correspondant à des alias,
// Nous pouvons utiliser les alias pour récupérer leurs clés respectives. Nous allons d'abord vérifier la validité des alias.
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

// 3 - Utiliser un alias valide :
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - Passez « null » comme alias afin d'utiliser le premier alias disponible qui renvoie une clé privée :
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Voir également

* class [CertificateHolder](../)
* espace de noms [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* Assemblée [Aspose.Words](../../../)
