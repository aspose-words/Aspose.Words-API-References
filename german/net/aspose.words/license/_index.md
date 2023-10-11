---
title: Class License
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.License klas. Stellt Methoden zur Lizenzierung der Komponente bereit.
type: docs
weight: 3420
url: /de/net/aspose.words/license/
---
## License class

Stellt Methoden zur Lizenzierung der Komponente bereit.

Um mehr zu erfahren, besuchen Sie die[Lizenzierung und Abonnement](https://docs.aspose.com/words/net/licensing/) Dokumentationsartikel.

```csharp
public class License
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [License](license/)() | Initialisiert eine neue Instanz dieser Klasse. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [SetLicense](../../aspose.words/license/setlicense/#setlicense)(Stream) | Lizenziert die Komponente. |
| [SetLicense](../../aspose.words/license/setlicense/#setlicense_1)(string) | Lizenziert die Komponente. |

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

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)


