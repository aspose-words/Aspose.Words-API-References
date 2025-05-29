---
title: CertificateHolder.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words für .NET
description: Erstellen Sie mühelos ein CertificateHolder-Objekt aus einem PKCS12-Byte-Array und einem Passwort. Vereinfachen Sie die Zertifikatsverwaltung mit unserer intuitiven Methode.
type: docs
weight: 10
url: /de/net/aspose.words.digitalsignatures/certificateholder/create/
---
## Create(*byte[], SecureString*) {#create}

Erstellt[`CertificateHolder`](../) Objekt, das ein Byte-Array des PKCS12-Speichers und sein Passwort verwendet.

```csharp
public static CertificateHolder Create(byte[] certBytes, SecureString password)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| certBytes | Byte[] | Ein Byte-Array, das Daten aus einem X.509-Zertifikat enthält. |
| password | SecureString | Das für den Zugriff auf die X.509-Zertifikatsdaten erforderliche Kennwort. |

### Rückgabewert

Ein Beispiel für[`CertificateHolder`](../)

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| InvalidParameterException | Ausgelöst, wenn*certBytes* Ist`null` |
| InvalidParameterException | Ausgelöst, wenn*password* Ist`null` |
| SecurityException | Wird ausgelöst, wenn der PKCS12-Speicher keine Aliase enthält |
| IOException | Wird ausgelöst, wenn ein falsches Passwort oder eine beschädigte Datei vorliegt. |

## Beispiele

Zeigt, wie CertificateHolder-Objekte erstellt werden.

```csharp
// Unten sind vier Möglichkeiten zum Erstellen von CertificateHolder-Objekten aufgeführt.
// 1 – Laden Sie eine PKCS#12-Datei in ein Byte-Array und wenden Sie ihr Passwort an:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - Laden Sie eine PKCS#12-Datei in ein Byte-Array und wenden Sie ein sicheres Passwort an:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Wenn das Zertifikat private Schlüssel hat, die Aliasnamen entsprechen,
// Wir können die Aliase verwenden, um ihre jeweiligen Schlüssel abzurufen. Zuerst prüfen wir, ob gültige Aliase vorhanden sind.
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

// 3 - Verwenden Sie einen gültigen Alias:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - Übergeben Sie „null“ als Alias, um den ersten verfügbaren Alias zu verwenden, der einen privaten Schlüssel zurückgibt:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Siehe auch

* class [CertificateHolder](../)
* namensraum [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* Montage [Aspose.Words](../../../)

---

## Create(*byte[], string*) {#create_1}

Erstellt[`CertificateHolder`](../) Objekt, das ein Byte-Array des PKCS12-Speichers und sein Passwort verwendet.

```csharp
public static CertificateHolder Create(byte[] certBytes, string password)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| certBytes | Byte[] | Ein Byte-Array, das Daten aus einem X.509-Zertifikat enthält. |
| password | String | Das für den Zugriff auf die X.509-Zertifikatsdaten erforderliche Kennwort. |

### Rückgabewert

Ein Beispiel für[`CertificateHolder`](../)

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| InvalidParameterException | Ausgelöst, wenn*certBytes* Ist`null` |
| InvalidParameterException | Ausgelöst, wenn*password* Ist`null` |
| SecurityException | Wird ausgelöst, wenn der PKCS12-Speicher keine Aliase enthält |
| IOException | Wird ausgelöst, wenn ein falsches Passwort oder eine beschädigte Datei vorliegt. |

## Beispiele

Zeigt, wie CertificateHolder-Objekte erstellt werden.

```csharp
// Unten sind vier Möglichkeiten zum Erstellen von CertificateHolder-Objekten aufgeführt.
// 1 – Laden Sie eine PKCS#12-Datei in ein Byte-Array und wenden Sie ihr Passwort an:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - Laden Sie eine PKCS#12-Datei in ein Byte-Array und wenden Sie ein sicheres Passwort an:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Wenn das Zertifikat private Schlüssel hat, die Aliasnamen entsprechen,
// Wir können die Aliase verwenden, um ihre jeweiligen Schlüssel abzurufen. Zuerst prüfen wir, ob gültige Aliase vorhanden sind.
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

// 3 - Verwenden Sie einen gültigen Alias:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - Übergeben Sie „null“ als Alias, um den ersten verfügbaren Alias zu verwenden, der einen privaten Schlüssel zurückgibt:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Siehe auch

* class [CertificateHolder](../)
* namensraum [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* Montage [Aspose.Words](../../../)

---

## Create(*string, string*) {#create_2}

Erstellt[`CertificateHolder`](../)Objekt mit Pfad zum PKCS12-Speicher und dessen Kennwort.

```csharp
public static CertificateHolder Create(string fileName, string password)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Der Name einer Zertifikatsdatei. |
| password | String | Das für den Zugriff auf die X.509-Zertifikatsdaten erforderliche Kennwort. |

### Rückgabewert

Ein Beispiel für[`CertificateHolder`](../)

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| InvalidParameterException | Ausgelöst, wenn*fileName* Ist`null` |
| InvalidParameterException | Ausgelöst, wenn*password* Ist`null` |
| SecurityException | Wird ausgelöst, wenn der PKCS12-Speicher keine Aliase enthält |
| IOException | Wird ausgelöst, wenn ein falsches Passwort oder eine beschädigte Datei vorliegt. |

## Beispiele

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

// Über einen Dateistream ein unsigniertes Dokument aus dem lokalen Dateisystem holen,
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

* class [CertificateHolder](../)
* namensraum [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* Montage [Aspose.Words](../../../)

---

## Create(*string, string, string*) {#create_3}

Erstellt[`CertificateHolder`](../) Objekt mit Pfad zum PKCS12-Speicher, seinem Passwort und dem Alias, mit dem der private Schlüssel und das Zertifikat gefunden werden.

```csharp
public static CertificateHolder Create(string fileName, string password, string alias)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Der Name einer Zertifikatsdatei. |
| password | String | Das für den Zugriff auf die X.509-Zertifikatsdaten erforderliche Kennwort. |
| alias | String | Der zugehörige Alias für ein Zertifikat und dessen privaten Schlüssel |

### Rückgabewert

Ein Beispiel für[`CertificateHolder`](../)

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| InvalidParameterException | Ausgelöst, wenn*fileName* Ist`null` |
| InvalidParameterException | Ausgelöst, wenn*password* Ist`null` |
| SecurityException | Wird ausgelöst, wenn der PKCS12-Speicher keine Aliase enthält |
| IOException | Wird ausgelöst, wenn ein falsches Passwort oder eine beschädigte Datei vorliegt. |
| SecurityException | Wird ausgelöst, wenn kein privater Schlüssel mit dem angegebenen Alias vorhanden ist |

## Beispiele

Zeigt, wie CertificateHolder-Objekte erstellt werden.

```csharp
// Unten sind vier Möglichkeiten zum Erstellen von CertificateHolder-Objekten aufgeführt.
// 1 – Laden Sie eine PKCS#12-Datei in ein Byte-Array und wenden Sie ihr Passwort an:
byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder.Create(certBytes, "aw");

// 2 - Laden Sie eine PKCS#12-Datei in ein Byte-Array und wenden Sie ein sicheres Passwort an:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
CertificateHolder.Create(certBytes, password);

// Wenn das Zertifikat private Schlüssel hat, die Aliasnamen entsprechen,
// Wir können die Aliase verwenden, um ihre jeweiligen Schlüssel abzurufen. Zuerst prüfen wir, ob gültige Aliase vorhanden sind.
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

// 3 - Verwenden Sie einen gültigen Alias:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 - Übergeben Sie „null“ als Alias, um den ersten verfügbaren Alias zu verwenden, der einen privaten Schlüssel zurückgibt:
CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
```

### Siehe auch

* class [CertificateHolder](../)
* namensraum [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* Montage [Aspose.Words](../../../)
