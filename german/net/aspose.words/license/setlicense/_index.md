---
title: License.SetLicense
second_title: Aspose.Words für .NET-API-Referenz
description: License methode. Lizenziert die Komponente.
type: docs
weight: 20
url: /de/net/aspose.words/license/setlicense/
---
## SetLicense(string) {#setlicense_1}

Lizenziert die Komponente.

```csharp
public void SetLicense(string licenseName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| licenseName | String | Kann ein vollständiger oder kurzer Dateiname oder der Name einer eingebetteten Ressource sein. Verwenden Sie eine leere Zeichenfolge, um in den Auswertungsmodus zu wechseln. |

### Bemerkungen

Versucht, die Lizenz an den folgenden Orten zu finden:

1. Expliziter Pfad.

2. Der Ordner, der die Aspose-Komponentenbaugruppe enthält.

3. Der Ordner, der die aufrufende Assembly des Clients enthält.

4. Der Ordner, der die Eintrags-(Start-)Assembly enthält.

5. Eine eingebettete Ressource in der aufrufenden Assembly des Clients.

**Notiz:**Versucht im .NET Compact Framework, die Lizenz nur an diesen Orten zu finden:

1. Expliziter Pfad.

2. Eine eingebettete Ressource in der aufrufenden Assembly des Clients.

### Beispiele

Zeigt, wie eine Lizenz für Aspose.Words mithilfe einer Lizenzdatei im lokalen Dateisystem initialisiert wird.

```csharp
// Legen Sie die Lizenz für unser Aspose.Words-Produkt fest, indem Sie den Dateinamen des lokalen Dateisystems einer gültigen Lizenzdatei übergeben.
string licenseFileName = Path.Combine(LicenseDir, "Aspose.Words.NET.lic");

License license = new License();
license.SetLicense(licenseFileName);

// Erstellen Sie eine Kopie unserer Lizenzdatei im Binärordner unserer Anwendung.
string licenseCopyFileName = Path.Combine(AssemblyDir, "Aspose.Words.NET.lic");
File.Copy(licenseFileName, licenseCopyFileName);

// Wenn wir den Namen einer Datei ohne Pfad übergeben,
// SetLicense durchsucht mehrere lokale Dateisystemspeicherorte nach dieser Datei.
// Einer dieser Speicherorte ist der Ordner „bin“, der eine Kopie unserer Lizenzdatei enthält.
license.SetLicense("Aspose.Words.NET.lic");
```

### Siehe auch

* class [License](../)
* namensraum [Aspose.Words](../../license/)
* Montage [Aspose.Words](../../../)

---

## SetLicense(Stream) {#setlicense}

Lizenziert die Komponente.

```csharp
public void SetLicense(Stream stream)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| stream | Stream | Ein Stream, der die Lizenz enthält. |

### Bemerkungen

Verwenden Sie diese Methode, um eine Lizenz aus einem Stream zu laden.

### Beispiele

Zeigt, wie eine Lizenz für Aspose.Words aus einem Stream initialisiert wird.

```csharp
// Legen Sie die Lizenz für unser Aspose.Words-Produkt fest, indem Sie einen Stream für eine gültige Lizenzdatei in unserem lokalen Dateisystem übergeben.
using (Stream myStream = File.OpenRead(Path.Combine(LicenseDir, "Aspose.Words.NET.lic")))
{
    License license = new License();
    license.SetLicense(myStream);
}
```

### Siehe auch

* class [License](../)
* namensraum [Aspose.Words](../../license/)
* Montage [Aspose.Words](../../../)


