---
title: CertificateHolder.Create
second_title: Aspose.Words für .NET-API-Referenz
description: CertificateHolder methode. ErstelltCertificateHolder Objekt unter Verwendung des ByteArrays des PKCS12Speichers und seines Passworts.
type: docs
weight: 10
url: /de/net/aspose.words.digitalsignatures/certificateholder/create/
---
## Create(byte[], SecureString) {#create}

Erstellt[`CertificateHolder`](../) Objekt unter Verwendung des Byte-Arrays des PKCS12-Speichers und seines Passworts.

```csharp
public static CertificateHolder Create(byte[] certBytes, SecureString password)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| certBytes | Byte[] | Ein Byte-Array, das Daten aus einem X.509-Zertifikat enthält. |
| password | SecureString | Das für den Zugriff auf die X.509-Zertifikatsdaten erforderliche Passwort. |

### Rückgabewert

Ein Beispiel für[`CertificateHolder`](../)

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| InvalidParameterException | Wird geworfen, wenn*certBytes* Ist`Null` |
| InvalidParameterException | Wird geworfen, wenn*password* Ist`Null` |
| SecurityException | Wird ausgelöst, wenn der PKCS12-Speicher keine Aliase enthält |
| IOException | Wird ausgelöst, wenn das Passwort falsch ist oder die Datei beschädigt ist. |

### Beispiele

Zeigt, wie CertificateHolder-Objekte erstellt werden.

```csharp
// Nachfolgend finden Sie vier Möglichkeiten zum Erstellen von CertificateHolder-Objekten.
// 1 – Laden Sie eine PKCS #12-Datei in ein Byte-Array und wenden Sie ihr Passwort an:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 – Laden Sie eine PKCS #12-Datei in ein Byte-Array und wenden Sie ein sicheres Passwort an:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Wenn das Zertifikat private Schlüssel hat, die Aliasen entsprechen,
// Wir können die Aliase verwenden, um ihre jeweiligen Schlüssel abzurufen. Zuerst prüfen wir, ob gültige Aliase vorhanden sind.
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

// 3 – Verwenden Sie einen gültigen Alias:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 – Übergeben Sie „null“ als Alias, um den ersten verfügbaren Alias zu verwenden, der einen privaten Schlüssel zurückgibt:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Siehe auch

* class [CertificateHolder](../)
* namensraum [Aspose.Words.DigitalSignatures](../../certificateholder/)
* Montage [Aspose.Words](../../../)

---

## Create(byte[], string) {#create_1}

Erstellt[`CertificateHolder`](../) Objekt unter Verwendung des Byte-Arrays des PKCS12-Speichers und seines Passworts.

```csharp
public static CertificateHolder Create(byte[] certBytes, string password)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| certBytes | Byte[] | Ein Byte-Array, das Daten aus einem X.509-Zertifikat enthält. |
| password | String | Das für den Zugriff auf die X.509-Zertifikatsdaten erforderliche Passwort. |

### Rückgabewert

Ein Beispiel für[`CertificateHolder`](../)

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| InvalidParameterException | Wird geworfen, wenn*certBytes* Ist`Null` |
| InvalidParameterException | Wird geworfen, wenn*password* Ist`Null` |
| SecurityException | Wird ausgelöst, wenn der PKCS12-Speicher keine Aliase enthält |
| IOException | Wird ausgelöst, wenn das Passwort falsch ist oder die Datei beschädigt ist. |

### Beispiele

Zeigt, wie CertificateHolder-Objekte erstellt werden.

```csharp
// Nachfolgend finden Sie vier Möglichkeiten zum Erstellen von CertificateHolder-Objekten.
// 1 – Laden Sie eine PKCS #12-Datei in ein Byte-Array und wenden Sie ihr Passwort an:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 – Laden Sie eine PKCS #12-Datei in ein Byte-Array und wenden Sie ein sicheres Passwort an:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Wenn das Zertifikat private Schlüssel hat, die Aliasen entsprechen,
// Wir können die Aliase verwenden, um ihre jeweiligen Schlüssel abzurufen. Zuerst prüfen wir, ob gültige Aliase vorhanden sind.
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

// 3 – Verwenden Sie einen gültigen Alias:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 – Übergeben Sie „null“ als Alias, um den ersten verfügbaren Alias zu verwenden, der einen privaten Schlüssel zurückgibt:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Siehe auch

* class [CertificateHolder](../)
* namensraum [Aspose.Words.DigitalSignatures](../../certificateholder/)
* Montage [Aspose.Words](../../../)

---

## Create(string, string) {#create_2}

Erstellt[`CertificateHolder`](../) Objekt unter Verwendung des Pfads zum PKCS12-Speicher und seines Passworts.

```csharp
public static CertificateHolder Create(string fileName, string password)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Der Name einer Zertifikatsdatei. |
| password | String | Das für den Zugriff auf die X.509-Zertifikatsdaten erforderliche Passwort. |

### Rückgabewert

Ein Beispiel für[`CertificateHolder`](../)

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| InvalidParameterException | Wird geworfen, wenn*fileName* Ist`Null` |
| InvalidParameterException | Wird geworfen, wenn*password* Ist`Null` |
| SecurityException | Wird ausgelöst, wenn der PKCS12-Speicher keine Aliase enthält |
| IOException | Wird ausgelöst, wenn das Passwort falsch ist oder die Datei beschädigt ist. |

### Beispiele

Zeigt, wie man Dokumente digital signiert.

```csharp
// Erstellen Sie ein X.509-Zertifikat aus einem PKCS#12-Speicher, das einen privaten Schlüssel enthalten sollte.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Erstellen Sie einen Kommentar und ein Datum, das mit unserer neuen digitalen Signatur angewendet wird.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// Über einen Dateistream ein unsigniertes Dokument aus dem lokalen Dateisystem übernehmen,
// dann eine signierte Kopie davon erstellen, die durch den Dateinamen des Ausgabedateistreams bestimmt wird.
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

### Siehe auch

* class [CertificateHolder](../)
* namensraum [Aspose.Words.DigitalSignatures](../../certificateholder/)
* Montage [Aspose.Words](../../../)

---

## Create(string, string, string) {#create_3}

Erstellt[`CertificateHolder`](../) Objekt unter Verwendung des Pfads zum PKCS12-Speicher, seines Passworts und des Alias, mit dem der private Schlüssel und das Zertifikat gefunden werden.

```csharp
public static CertificateHolder Create(string fileName, string password, string alias)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Der Name einer Zertifikatsdatei. |
| password | String | Das für den Zugriff auf die X.509-Zertifikatsdaten erforderliche Passwort. |
| alias | String | Der zugehörige Alias für ein Zertifikat und seinen privaten Schlüssel |

### Rückgabewert

Ein Beispiel für[`CertificateHolder`](../)

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| InvalidParameterException | Wird geworfen, wenn*fileName* Ist`Null` |
| InvalidParameterException | Wird geworfen, wenn*password* Ist`Null` |
| SecurityException | Wird ausgelöst, wenn der PKCS12-Speicher keine Aliase enthält |
| IOException | Wird ausgelöst, wenn das Passwort falsch ist oder die Datei beschädigt ist. |
| SecurityException | Wird ausgelöst, wenn kein privater Schlüssel mit dem angegebenen Alias vorhanden ist |

### Beispiele

Zeigt, wie CertificateHolder-Objekte erstellt werden.

```csharp
// Nachfolgend finden Sie vier Möglichkeiten zum Erstellen von CertificateHolder-Objekten.
// 1 – Laden Sie eine PKCS #12-Datei in ein Byte-Array und wenden Sie ihr Passwort an:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 – Laden Sie eine PKCS #12-Datei in ein Byte-Array und wenden Sie ein sicheres Passwort an:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Wenn das Zertifikat private Schlüssel hat, die Aliasen entsprechen,
// Wir können die Aliase verwenden, um ihre jeweiligen Schlüssel abzurufen. Zuerst prüfen wir, ob gültige Aliase vorhanden sind.
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

// 3 – Verwenden Sie einen gültigen Alias:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 – Übergeben Sie „null“ als Alias, um den ersten verfügbaren Alias zu verwenden, der einen privaten Schlüssel zurückgibt:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Siehe auch

* class [CertificateHolder](../)
* namensraum [Aspose.Words.DigitalSignatures](../../certificateholder/)
* Montage [Aspose.Words](../../../)


