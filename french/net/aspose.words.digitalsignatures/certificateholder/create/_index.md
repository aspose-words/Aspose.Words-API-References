---
title: Create
second_title: Référence de l'API Aspose.Words pour .NET
description: Crée un objet CertificateHolder à laide du tableau doctets du magasin PKCS12 et de son mot de passe.
type: docs
weight: 10
url: /fr/net/aspose.words.digitalsignatures/certificateholder/create/
---
## Create(byte[], SecureString) {#create}

Crée un objet CertificateHolder à l'aide du tableau d'octets du magasin PKCS12 et de son mot de passe.

```csharp
public static CertificateHolder Create(byte[] certBytes, SecureString password)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| certBytes | Byte[] | Tableau d'octets contenant les données d'un certificat X.509. |
| password | SecureString | Mot de passe requis pour accéder aux données du certificat X.509. |

### Return_Value

Une instance de CertificateHolder

### Exceptions

| exception | condition |
| --- | --- |
| InvalidParameterException | Jeté si **certBytes** est nul |
| InvalidParameterException | Jeté si **le mot de passe** est nul |
| SecurityException | Levé si le magasin PKCS12 ne contient aucun alias |
| IOException | Lève s'il y a un mauvais mot de passe ou un fichier corrompu. |

### Exemples

Montre comment créer des objets CertificateHolder.

```csharp
// Vous trouverez ci-dessous quatre façons de créer des objets CertificateHolder.
// 1 - Charge un fichier PKCS #12 dans un tableau d'octets et applique son mot de passe :
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - Chargez un fichier PKCS #12 dans un tableau d'octets et appliquez un mot de passe sécurisé :
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Si le certificat possède des clés privées correspondant à des alias,
// nous pouvons utiliser les alias pour récupérer leurs clés respectives. Tout d'abord, nous allons vérifier les alias valides.
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

// 3 - Utilisez un alias valide :
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - Passez "null" comme alias afin d'utiliser le premier alias disponible qui renvoie une clé privée :
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Voir également

* class [CertificateHolder](../)
* espace de noms [Aspose.Words.DigitalSignatures](../../certificateholder/)
* Assemblée [Aspose.Words](../../../)

---

## Create(byte[], string) {#create_1}

Crée un objet CertificateHolder à l'aide du tableau d'octets du magasin PKCS12 et de son mot de passe.

```csharp
public static CertificateHolder Create(byte[] certBytes, string password)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| certBytes | Byte[] | Tableau d'octets contenant les données d'un certificat X.509. |
| password | String | Mot de passe requis pour accéder aux données du certificat X.509. |

### Return_Value

Une instance de CertificateHolder

### Exceptions

| exception | condition |
| --- | --- |
| InvalidParameterException | Jeté si **certBytes** est nul |
| InvalidParameterException | Jeté si **le mot de passe** est nul |
| SecurityException | Levé si le magasin PKCS12 ne contient aucun alias |
| IOException | Lève s'il y a un mauvais mot de passe ou un fichier corrompu. |

### Exemples

Montre comment créer des objets CertificateHolder.

```csharp
// Vous trouverez ci-dessous quatre façons de créer des objets CertificateHolder.
// 1 - Charge un fichier PKCS #12 dans un tableau d'octets et applique son mot de passe :
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - Chargez un fichier PKCS #12 dans un tableau d'octets et appliquez un mot de passe sécurisé :
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Si le certificat possède des clés privées correspondant à des alias,
// nous pouvons utiliser les alias pour récupérer leurs clés respectives. Tout d'abord, nous allons vérifier les alias valides.
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

// 3 - Utilisez un alias valide :
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - Passez "null" comme alias afin d'utiliser le premier alias disponible qui renvoie une clé privée :
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Voir également

* class [CertificateHolder](../)
* espace de noms [Aspose.Words.DigitalSignatures](../../certificateholder/)
* Assemblée [Aspose.Words](../../../)

---

## Create(string, string) {#create_2}

Crée un objet CertificateHolder en utilisant le chemin d'accès au magasin PKCS12 et son mot de passe.

```csharp
public static CertificateHolder Create(string fileName, string password)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fileName | String | Le nom d'un fichier de certificat. |
| password | String | Mot de passe requis pour accéder aux données du certificat X.509. |

### Return_Value

Une instance de CertificateHolder

### Exceptions

| exception | condition |
| --- | --- |
| InvalidParameterException | Jeté si **nom de fichier** est nul |
| InvalidParameterException | Jeté si **le mot de passe** est nul |
| SecurityException | Levé si le magasin PKCS12 ne contient aucun alias |
| IOException | Lève s'il y a un mauvais mot de passe ou un fichier corrompu. |

### Exemples

Montre comment signer numériquement des documents.

```csharp
// Crée un certificat X.509 à partir d'un magasin PKCS#12, qui doit contenir une clé privée.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Créez un commentaire et une date qui seront appliqués avec notre nouvelle signature numérique.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// Prend un document non signé du système de fichiers local via un flux de fichiers,
// puis créez une copie signée de celui-ci déterminée par le nom de fichier du flux de fichier de sortie.
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
* espace de noms [Aspose.Words.DigitalSignatures](../../certificateholder/)
* Assemblée [Aspose.Words](../../../)

---

## Create(string, string, string) {#create_3}

Crée un objet CertificateHolder en utilisant le chemin d'accès au magasin PKCS12, son mot de passe et l'alias en utilisant la clé privée et le certificat qui seront trouvés.

```csharp
public static CertificateHolder Create(string fileName, string password, string alias)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fileName | String | Le nom d'un fichier de certificat. |
| password | String | Mot de passe requis pour accéder aux données du certificat X.509. |
| alias | String | L'alias associé pour un certificat et sa clé privée |

### Return_Value

Une instance de CertificateHolder

### Exceptions

| exception | condition |
| --- | --- |
| InvalidParameterException | Jeté si **nom de fichier** est nul |
| InvalidParameterException | Jeté si **le mot de passe** est nul |
| SecurityException | Levé si le magasin PKCS12 ne contient aucun alias |
| IOException | Lève s'il y a un mauvais mot de passe ou un fichier corrompu. |
| SecurityException | Levé s'il n'y a pas de clé privée avec l'alias donné |

### Exemples

Montre comment créer des objets CertificateHolder.

```csharp
// Vous trouverez ci-dessous quatre façons de créer des objets CertificateHolder.
// 1 - Charge un fichier PKCS #12 dans un tableau d'octets et applique son mot de passe :
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - Chargez un fichier PKCS #12 dans un tableau d'octets et appliquez un mot de passe sécurisé :
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Si le certificat possède des clés privées correspondant à des alias,
// nous pouvons utiliser les alias pour récupérer leurs clés respectives. Tout d'abord, nous allons vérifier les alias valides.
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

// 3 - Utilisez un alias valide :
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - Passez "null" comme alias afin d'utiliser le premier alias disponible qui renvoie une clé privée :
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Voir également

* class [CertificateHolder](../)
* espace de noms [Aspose.Words.DigitalSignatures](../../certificateholder/)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
