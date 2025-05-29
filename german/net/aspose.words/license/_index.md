---
title: License Class
linktitle: License
articleTitle: License
second_title: Aspose.Words für .NET
description: Entfesseln Sie das volle Potenzial von Aspose.Words mit unserer Lizenzklasse. Verwalten Sie Lizenzen ganz einfach für eine reibungslose Dokumentenverarbeitung und erweiterte Funktionalität.
type: docs
weight: 3870
url: /de/net/aspose.words/license/
---
## License class

Bietet Methoden zum Lizenzieren der Komponente.

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
| [SetLicense](../../aspose.words/license/setlicense/#setlicense)(*Stream*) | Lizenziert die Komponente. |
| [SetLicense](../../aspose.words/license/setlicense/#setlicense_1)(*string*) | Lizenziert die Komponente. |

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

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
