---
title: License
linktitle: License
articleTitle: License
second_title: Aspose.Words für .NET
description: Erstellen und verwalten Sie Lizenzen mühelos mit unserer Konstruktorklasse. Vereinfachen Sie Ihren Lizenzierungsprozess und steigern Sie die Effizienz noch heute!
type: docs
weight: 10
url: /de/net/aspose.words/license/license/
---
## License constructor

Initialisiert eine neue Instanz dieser Klasse.

```csharp
public License()
```

## Beispiele

Zeigt, wie eine Lizenz für Aspose.Words mithilfe einer Lizenzdatei im lokalen Dateisystem initialisiert wird.

```csharp
// Legen Sie die Lizenz für unser Aspose.Words-Produkt fest, indem Sie den Dateinamen einer gültigen Lizenzdatei im lokalen Dateisystem übergeben.
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
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
