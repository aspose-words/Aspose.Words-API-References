---
title: CertificateHolder.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words para .NET
description: Cree fácilmente un objeto CertificateHolder a partir de una matriz de bytes PKCS12 y una contraseña. Simplifique la gestión de certificados con nuestro método intuitivo.
type: docs
weight: 10
url: /es/net/aspose.words.digitalsignatures/certificateholder/create/
---
## Create(*byte[], SecureString*) {#create}

Crea[`CertificateHolder`](../) objeto que utiliza la matriz de bytes del almacén PKCS12 y su contraseña.

```csharp
public static CertificateHolder Create(byte[] certBytes, SecureString password)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| certBytes | Byte[] | Una matriz de bytes que contiene datos de un certificado X.509. |
| password | SecureString | La contraseña necesaria para acceder a los datos del certificado X.509. |

### Valor_devuelto

Un ejemplo de[`CertificateHolder`](../)

### Excepciones

| excepción | condición |
| --- | --- |
| InvalidParameterException | Lanzado si*certBytes* es`nulo` |
| InvalidParameterException | Lanzado si*password* es`nulo` |
| SecurityException | Se lanza si el almacén PKCS12 no contiene alias |
| IOException | Se lanza si hay una contraseña incorrecta o un archivo dañado. |

## Ejemplos

Muestra cómo crear objetos CertificateHolder.

```csharp
// A continuación se muestran cuatro formas de crear objetos CertificateHolder.
// 1 - Cargar un archivo PKCS #12 en una matriz de bytes y aplicar su contraseña:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - Cargue un archivo PKCS #12 en una matriz de bytes y aplique una contraseña segura:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Si el certificado tiene claves privadas correspondientes a alias,
Podemos usar los alias para obtener sus respectivas claves. Primero, comprobaremos si los alias son válidos.
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

// 3 - Utilice un alias válido:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - Pase "null" como alias para utilizar el primer alias disponible que devuelva una clave privada:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Ver también

* class [CertificateHolder](../)
* espacio de nombres [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* asamblea [Aspose.Words](../../../)

---

## Create(*byte[], string*) {#create_1}

Crea[`CertificateHolder`](../) objeto que utiliza la matriz de bytes del almacén PKCS12 y su contraseña.

```csharp
public static CertificateHolder Create(byte[] certBytes, string password)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| certBytes | Byte[] | Una matriz de bytes que contiene datos de un certificado X.509. |
| password | String | La contraseña necesaria para acceder a los datos del certificado X.509. |

### Valor_devuelto

Un ejemplo de[`CertificateHolder`](../)

### Excepciones

| excepción | condición |
| --- | --- |
| InvalidParameterException | Lanzado si*certBytes* es`nulo` |
| InvalidParameterException | Lanzado si*password* es`nulo` |
| SecurityException | Se lanza si el almacén PKCS12 no contiene alias |
| IOException | Se lanza si hay una contraseña incorrecta o un archivo dañado. |

## Ejemplos

Muestra cómo crear objetos CertificateHolder.

```csharp
// A continuación se muestran cuatro formas de crear objetos CertificateHolder.
// 1 - Cargar un archivo PKCS #12 en una matriz de bytes y aplicar su contraseña:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - Cargue un archivo PKCS #12 en una matriz de bytes y aplique una contraseña segura:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Si el certificado tiene claves privadas correspondientes a alias,
Podemos usar los alias para obtener sus respectivas claves. Primero, comprobaremos si los alias son válidos.
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

// 3 - Utilice un alias válido:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - Pase "null" como alias para utilizar el primer alias disponible que devuelva una clave privada:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Ver también

* class [CertificateHolder](../)
* espacio de nombres [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* asamblea [Aspose.Words](../../../)

---

## Create(*string, string*) {#create_2}

Crea[`CertificateHolder`](../)objeto que utiliza la ruta al almacén PKCS12 y su contraseña.

```csharp
public static CertificateHolder Create(string fileName, string password)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fileName | String | El nombre de un archivo de certificado. |
| password | String | La contraseña necesaria para acceder a los datos del certificado X.509. |

### Valor_devuelto

Un ejemplo de[`CertificateHolder`](../)

### Excepciones

| excepción | condición |
| --- | --- |
| InvalidParameterException | Lanzado si*fileName* es`nulo` |
| InvalidParameterException | Lanzado si*password* es`nulo` |
| SecurityException | Se lanza si el almacén PKCS12 no contiene alias |
| IOException | Se lanza si hay una contraseña incorrecta o un archivo dañado. |

## Ejemplos

Muestra cómo firmar documentos digitalmente.

```csharp
// Cree un certificado X.509 desde un almacén PKCS#12, que debe contener una clave privada.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Crea un comentario y una fecha que se aplicará con nuestra nueva firma digital.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// Tome un documento sin firmar del sistema de archivos local a través de un flujo de archivos,
// luego crea una copia firmada determinada por el nombre del archivo de flujo de salida.
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
* espacio de nombres [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* asamblea [Aspose.Words](../../../)

---

## Create(*string, string, string*) {#create_3}

Crea[`CertificateHolder`](../) objeto que utiliza la ruta al almacén PKCS12, su contraseña y el alias mediante el cual se encontrará la clave privada y el certificado.

```csharp
public static CertificateHolder Create(string fileName, string password, string alias)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fileName | String | El nombre de un archivo de certificado. |
| password | String | La contraseña necesaria para acceder a los datos del certificado X.509. |
| alias | String | El alias asociado a un certificado y su clave privada |

### Valor_devuelto

Un ejemplo de[`CertificateHolder`](../)

### Excepciones

| excepción | condición |
| --- | --- |
| InvalidParameterException | Lanzado si*fileName* es`nulo` |
| InvalidParameterException | Lanzado si*password* es`nulo` |
| SecurityException | Se lanza si el almacén PKCS12 no contiene alias |
| IOException | Se lanza si hay una contraseña incorrecta o un archivo dañado. |
| SecurityException | Se lanza si no hay una clave privada con el alias dado |

## Ejemplos

Muestra cómo crear objetos CertificateHolder.

```csharp
// A continuación se muestran cuatro formas de crear objetos CertificateHolder.
// 1 - Cargar un archivo PKCS #12 en una matriz de bytes y aplicar su contraseña:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - Cargue un archivo PKCS #12 en una matriz de bytes y aplique una contraseña segura:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Si el certificado tiene claves privadas correspondientes a alias,
Podemos usar los alias para obtener sus respectivas claves. Primero, comprobaremos si los alias son válidos.
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

// 3 - Utilice un alias válido:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - Pase "null" como alias para utilizar el primer alias disponible que devuelva una clave privada:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Ver también

* class [CertificateHolder](../)
* espacio de nombres [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* asamblea [Aspose.Words](../../../)
