---
title: Create
second_title: Referencia de API de Aspose.Words para .NET
description: Crea el objeto CertificateHolder utilizando la matriz de bytes del almacén PKCS12 y su contraseña.
type: docs
weight: 10
url: /es/net/aspose.words.digitalsignatures/certificateholder/create/
---
## Create(byte[], SecureString) {#create}

Crea el objeto CertificateHolder utilizando la matriz de bytes del almacén PKCS12 y su contraseña.

```csharp
public static CertificateHolder Create(byte[] certBytes, SecureString password)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| certBytes | Byte[] | Una matriz de bytes que contiene datos de un certificado X.509. |
| password | SecureString | La contraseña necesaria para acceder a los datos del certificado X.509. |

### Valor_devuelto

Una instancia de CertificateHolder

### Excepciones

| excepción | condición |
| --- | --- |
| InvalidParameterException | arrojado si **certBytes** es nulo |
| InvalidParameterException | arrojado si **clave** es nulo |
| SecurityException | Lanzado si la tienda PKCS12 no contiene alias |
| IOException | Lanzado si hay una contraseña incorrecta o un archivo dañado. |

### Ejemplos

Muestra cómo crear objetos CertificateHolder.

```csharp
// A continuación se muestran cuatro formas de crear objetos CertificateHolder.
// 1 - Cargue un archivo PKCS #12 en una matriz de bytes y aplique su contraseña:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - Cargue un archivo PKCS #12 en una matriz de bytes y aplique una contraseña segura:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Si el certificado tiene claves privadas correspondientes a alias,
// podemos usar los alias para obtener sus respectivas claves. Primero, buscaremos alias válidos.
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

// 3 - Usa un alias válido:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - Pase "null" como alias para usar el primer alias disponible que devuelva una clave privada:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Ver también

* class [CertificateHolder](../)
* espacio de nombres [Aspose.Words.DigitalSignatures](../../certificateholder/)
* asamblea [Aspose.Words](../../../)

---

## Create(byte[], string) {#create_1}

Crea el objeto CertificateHolder utilizando la matriz de bytes del almacén PKCS12 y su contraseña.

```csharp
public static CertificateHolder Create(byte[] certBytes, string password)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| certBytes | Byte[] | Una matriz de bytes que contiene datos de un certificado X.509. |
| password | String | La contraseña necesaria para acceder a los datos del certificado X.509. |

### Valor_devuelto

Una instancia de CertificateHolder

### Excepciones

| excepción | condición |
| --- | --- |
| InvalidParameterException | arrojado si **certBytes** es nulo |
| InvalidParameterException | arrojado si **clave** es nulo |
| SecurityException | Lanzado si la tienda PKCS12 no contiene alias |
| IOException | Lanzado si hay una contraseña incorrecta o un archivo dañado. |

### Ejemplos

Muestra cómo crear objetos CertificateHolder.

```csharp
// A continuación se muestran cuatro formas de crear objetos CertificateHolder.
// 1 - Cargue un archivo PKCS #12 en una matriz de bytes y aplique su contraseña:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - Cargue un archivo PKCS #12 en una matriz de bytes y aplique una contraseña segura:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Si el certificado tiene claves privadas correspondientes a alias,
// podemos usar los alias para obtener sus respectivas claves. Primero, buscaremos alias válidos.
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

// 3 - Usa un alias válido:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - Pase "null" como alias para usar el primer alias disponible que devuelva una clave privada:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Ver también

* class [CertificateHolder](../)
* espacio de nombres [Aspose.Words.DigitalSignatures](../../certificateholder/)
* asamblea [Aspose.Words](../../../)

---

## Create(string, string) {#create_2}

Crea el objeto CertificateHolder usando la ruta al almacén PKCS12 y su contraseña.

```csharp
public static CertificateHolder Create(string fileName, string password)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fileName | String | El nombre de un archivo de certificado. |
| password | String | La contraseña necesaria para acceder a los datos del certificado X.509. |

### Valor_devuelto

Una instancia de CertificateHolder

### Excepciones

| excepción | condición |
| --- | --- |
| InvalidParameterException | arrojado si **Nombre del archivo** es nulo |
| InvalidParameterException | arrojado si **clave** es nulo |
| SecurityException | Lanzado si la tienda PKCS12 no contiene alias |
| IOException | Lanzado si hay una contraseña incorrecta o un archivo dañado. |

### Ejemplos

Muestra cómo firmar documentos digitalmente.

```csharp
// Cree un certificado X.509 desde un almacén PKCS#12, que debe contener una clave privada.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Cree un comentario y una fecha que se aplicará con nuestra nueva firma digital.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// Tome un documento sin firmar del sistema de archivos local a través de un flujo de archivos,
// luego cree una copia firmada determinada por el nombre de archivo de la secuencia del archivo de salida.
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

### Ver también

* class [CertificateHolder](../)
* espacio de nombres [Aspose.Words.DigitalSignatures](../../certificateholder/)
* asamblea [Aspose.Words](../../../)

---

## Create(string, string, string) {#create_3}

Crea el objeto CertificateHolder usando la ruta al almacén PKCS12, su contraseña y el alias mediante el cual se encontrará la clave privada y el certificado.

```csharp
public static CertificateHolder Create(string fileName, string password, string alias)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fileName | String | El nombre de un archivo de certificado. |
| password | String | La contraseña necesaria para acceder a los datos del certificado X.509. |
| alias | String | El alias asociado para un certificado y su clave privada |

### Valor_devuelto

Una instancia de CertificateHolder

### Excepciones

| excepción | condición |
| --- | --- |
| InvalidParameterException | arrojado si **Nombre del archivo** es nulo |
| InvalidParameterException | arrojado si **clave** es nulo |
| SecurityException | Lanzado si la tienda PKCS12 no contiene alias |
| IOException | Lanzado si hay una contraseña incorrecta o un archivo dañado. |
| SecurityException | Lanzado si no hay una clave privada con el alias dado |

### Ejemplos

Muestra cómo crear objetos CertificateHolder.

```csharp
// A continuación se muestran cuatro formas de crear objetos CertificateHolder.
// 1 - Cargue un archivo PKCS #12 en una matriz de bytes y aplique su contraseña:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - Cargue un archivo PKCS #12 en una matriz de bytes y aplique una contraseña segura:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Si el certificado tiene claves privadas correspondientes a alias,
// podemos usar los alias para obtener sus respectivas claves. Primero, buscaremos alias válidos.
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

// 3 - Usa un alias válido:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - Pase "null" como alias para usar el primer alias disponible que devuelva una clave privada:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Ver también

* class [CertificateHolder](../)
* espacio de nombres [Aspose.Words.DigitalSignatures](../../certificateholder/)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
