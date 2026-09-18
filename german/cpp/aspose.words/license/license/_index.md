---
title: "Aspose::Words::License::License-Konstruktor"
linktitle: "License"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::License::License-Konstruktor. Initialisiert eine neue Instanz dieser Klasse in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words/license/license/
---
## License::License constructor


Initialisiert eine neue Instanz dieser Klasse.

```cpp
Aspose::Words::License::License()
```


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

* Class [License](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
