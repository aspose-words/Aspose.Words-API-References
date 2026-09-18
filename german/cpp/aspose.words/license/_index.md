---
title: "Aspose::Words::License class"
linktitle: "License"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::License class. Stellt Methoden zur Lizenzierung der Komponente bereit. Weitere Informationen finden Sie im Dokumentationsartikel zu C++."
type: docs
weight: 39000
url: /de/cpp/aspose.words/license/
---
## License class


Stellt Methoden zur Lizenzierung der Komponente bereit. Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [Licensing and Subscription](https://docs.aspose.com/words/cpp/licensing/).

```cpp
class License : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [License](./license/)() | Initialisiert eine neue Instanz dieser Klasse. |
| [SetLicense](./setlicense/)(const System::String\&) | Lizenziert die Komponente. |
| [SetLicense](./setlicense/)(const System::SharedPtr\<System::IO::Stream\>\&) | Lizenziert die Komponente. |
| [SetLicense](./setlicense/)(std::basic_istream\<CharType, Traits\>\&) |  |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie man eine Lizenz für Aspose.Words mit einer Lizenzdatei im lokalen Dateisystem initialisiert.
```cpp
System::String testLicenseFileName = u"Aspose.Words.Cpp.lic";

// Setzen Sie die Lizenz für unser Aspose.Words‑Produkt, indem Sie den Dateinamen einer gültigen Lizenzdatei im lokalen Dateisystem übergeben.
System::String licenseFileName = System::IO::Path::Combine(get_LicenseDir(), testLicenseFileName);

auto license = System::MakeObject<Aspose::Words::License>();
license->SetLicense(licenseFileName);

// Erstellen Sie eine Kopie unserer Lizenzdatei im Binärordner unserer Anwendung.
System::String licenseCopyFileName = System::IO::Path::Combine(get_AssemblyDir(), testLicenseFileName);
System::IO::File::Copy(licenseFileName, licenseCopyFileName);

// Wenn wir den Dateinamen ohne Pfad übergeben,
// wird SetLicense an mehreren Speicherorten im lokalen Dateisystem nach dieser Datei suchen.
// Einer dieser Speicherorte ist der "bin"‑Ordner, der eine Kopie unserer Lizenzdatei enthält.
license->SetLicense(testLicenseFileName);
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
