---
title: Create
second_title: Aspose.Words für .NET-API-Referenz
description: Erstellt ein CertificateHolder-Objekt mithilfe des Byte-Arrays des PKCS12-Speichers und seines Kennworts.
type: docs
weight: 10
url: /de/net/aspose.words.digitalsignatures/certificateholder/create/
---
## Create(byte[], SecureString) {#create}

Erstellt ein CertificateHolder-Objekt mithilfe des Byte-Arrays des PKCS12-Speichers und seines Kennworts.

```csharp
public static CertificateHolder Create(byte[] certBytes, SecureString password)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| certBytes | Byte[] | Ein Byte-Array, das Daten aus einem X.509-Zertifikat enthält. |
| password | SecureString | Das Kennwort, das für den Zugriff auf die X.509-Zertifikatsdaten erforderlich ist. |

### Rückgabewert

Eine Instanz von CertificateHolder

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| InvalidParameterException | Geworfen wenn **certBytes** ist Null |
| InvalidParameterException | Geworfen wenn **Passwort** ist Null |
| SecurityException | Wird ausgelöst, wenn der PKCS12-Speicher keine Aliase enthält |
| IOException | Wird ausgelöst, wenn ein falsches Passwort oder eine beschädigte Datei vorhanden ist. |

### Beispiele

Zeigt, wie CertificateHolder-Objekte erstellt werden.

```csharp
// Nachfolgend finden Sie vier Möglichkeiten zum Erstellen von CertificateHolder-Objekten.
// 1 - Laden Sie eine PKCS #12-Datei in ein Byte-Array und wenden Sie ihr Passwort an:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - Laden Sie eine PKCS #12-Datei in ein Byte-Array und wenden Sie ein sicheres Passwort an:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Wenn das Zertifikat private Schlüssel hat, die Aliassen entsprechen,
// Wir können die Aliase verwenden, um ihre jeweiligen Schlüssel abzurufen. Zuerst werden wir nach gültigen Aliasnamen suchen.
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

// 3 - Verwenden Sie einen gültigen Alias:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - Übergeben Sie "null" als Alias, um den ersten verfügbaren Alias zu verwenden, der einen privaten Schlüssel zurückgibt:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Siehe auch

* class [CertificateHolder](../../certificateholder)
* namensraum [Aspose.Words.DigitalSignatures](../../certificateholder)
* Montage [Aspose.Words](../../../)

---

## Create(byte[], string) {#create_1}

Erstellt ein CertificateHolder-Objekt mithilfe des Byte-Arrays des PKCS12-Speichers und seines Kennworts.

```csharp
public static CertificateHolder Create(byte[] certBytes, string password)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| certBytes | Byte[] | Ein Byte-Array, das Daten aus einem X.509-Zertifikat enthält. |
| password | String | Das Kennwort, das für den Zugriff auf die X.509-Zertifikatsdaten erforderlich ist. |

### Rückgabewert

Eine Instanz von CertificateHolder

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| InvalidParameterException | Geworfen wenn **certBytes** ist Null |
| InvalidParameterException | Geworfen wenn **Passwort** ist Null |
| SecurityException | Wird ausgelöst, wenn der PKCS12-Speicher keine Aliase enthält |
| IOException | Wird ausgelöst, wenn ein falsches Passwort oder eine beschädigte Datei vorhanden ist. |

### Beispiele

Zeigt, wie CertificateHolder-Objekte erstellt werden.

```csharp
// Nachfolgend finden Sie vier Möglichkeiten zum Erstellen von CertificateHolder-Objekten.
// 1 - Laden Sie eine PKCS #12-Datei in ein Byte-Array und wenden Sie ihr Passwort an:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - Laden Sie eine PKCS #12-Datei in ein Byte-Array und wenden Sie ein sicheres Passwort an:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Wenn das Zertifikat private Schlüssel hat, die Aliassen entsprechen,
// Wir können die Aliase verwenden, um ihre jeweiligen Schlüssel abzurufen. Zuerst werden wir nach gültigen Aliasnamen suchen.
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

// 3 - Verwenden Sie einen gültigen Alias:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - Übergeben Sie "null" als Alias, um den ersten verfügbaren Alias zu verwenden, der einen privaten Schlüssel zurückgibt:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Siehe auch

* class [CertificateHolder](../../certificateholder)
* namensraum [Aspose.Words.DigitalSignatures](../../certificateholder)
* Montage [Aspose.Words](../../../)

---

## Create(string, string) {#create_2}

Erstellt ein CertificateHolder-Objekt unter Verwendung des Pfads zum PKCS12-Speicher und seines Kennworts.

```csharp
public static CertificateHolder Create(string fileName, string password)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Der Name einer Zertifikatsdatei. |
| password | String | Das Kennwort, das für den Zugriff auf die X.509-Zertifikatsdaten erforderlich ist. |

### Rückgabewert

Eine Instanz von CertificateHolder

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| InvalidParameterException | Geworfen wenn **Dateiname** ist Null |
| InvalidParameterException | Geworfen wenn **Passwort** ist Null |
| SecurityException | Wird ausgelöst, wenn der PKCS12-Speicher keine Aliase enthält |
| IOException | Wird ausgelöst, wenn ein falsches Passwort oder eine beschädigte Datei vorhanden ist. |

### Beispiele

Zeigt, wie Dokumente digital signiert werden.

```csharp
// Erstellen Sie ein X.509-Zertifikat aus einem PKCS#12-Speicher, das einen privaten Schlüssel enthalten sollte.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Erstellen Sie einen Kommentar und ein Datum, die mit unserer neuen digitalen Signatur angewendet werden.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// Nimm ein unsigniertes Dokument aus dem lokalen Dateisystem über einen Dateistream,
// Erstellen Sie dann eine signierte Kopie davon, die durch den Dateinamen des Ausgabedateistreams bestimmt wird.
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

### Siehe auch

* class [CertificateHolder](../../certificateholder)
* namensraum [Aspose.Words.DigitalSignatures](../../certificateholder)
* Montage [Aspose.Words](../../../)

---

## Create(string, string, string) {#create_3}

Erstellt ein CertificateHolder-Objekt unter Verwendung des Pfads zum PKCS12-Speicher, seines Passworts und des Alias, anhand dessen der private Schlüssel und das Zertifikat gefunden werden.

```csharp
public static CertificateHolder Create(string fileName, string password, string alias)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Der Name einer Zertifikatsdatei. |
| password | String | Das Kennwort, das für den Zugriff auf die X.509-Zertifikatsdaten erforderlich ist. |
| alias | String | Der zugeordnete Alias für ein Zertifikat und seinen privaten Schlüssel |

### Rückgabewert

Eine Instanz von CertificateHolder

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| InvalidParameterException | Geworfen wenn **Dateiname** ist Null |
| InvalidParameterException | Geworfen wenn **Passwort** ist Null |
| SecurityException | Wird ausgelöst, wenn der PKCS12-Speicher keine Aliase enthält |
| IOException | Wird ausgelöst, wenn ein falsches Passwort oder eine beschädigte Datei vorhanden ist. |
| SecurityException | Wird ausgelöst, wenn kein privater Schlüssel mit dem angegebenen Alias vorhanden ist |

### Beispiele

Zeigt, wie CertificateHolder-Objekte erstellt werden.

```csharp
// Nachfolgend finden Sie vier Möglichkeiten zum Erstellen von CertificateHolder-Objekten.
// 1 - Laden Sie eine PKCS #12-Datei in ein Byte-Array und wenden Sie ihr Passwort an:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - Laden Sie eine PKCS #12-Datei in ein Byte-Array und wenden Sie ein sicheres Passwort an:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Wenn das Zertifikat private Schlüssel hat, die Aliassen entsprechen,
// Wir können die Aliase verwenden, um ihre jeweiligen Schlüssel abzurufen. Zuerst werden wir nach gültigen Aliasnamen suchen.
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

// 3 - Verwenden Sie einen gültigen Alias:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - Übergeben Sie "null" als Alias, um den ersten verfügbaren Alias zu verwenden, der einen privaten Schlüssel zurückgibt:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Siehe auch

* class [CertificateHolder](../../certificateholder)
* namensraum [Aspose.Words.DigitalSignatures](../../certificateholder)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
