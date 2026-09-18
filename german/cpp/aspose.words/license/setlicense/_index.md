---
title: "Aspose::Words::License::SetLicense-Methode"
linktitle: "SetLicense"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::License::SetLicense-Methode. Lizenziert die Komponente in C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words/license/setlicense/
---
## License::SetLicense(const System::SharedPtr\<System::IO::Stream\>\&) method


Lizenziert die Komponente.

```cpp
void Aspose::Words::License::SetLicense(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Datenstrom | const System::SharedPtr\<System::IO::Stream\>\& | Ein Stream, der die Lizenz enthält. |
## Hinweise


Verwenden Sie diese Methode, um eine Lizenz aus einem Stream zu laden.

## Beispiele



Zeigt, wie man eine Lizenz für Aspose.Words aus einem Stream initialisiert.
```cpp
System::String testLicenseFileName = u"Aspose.Words.Cpp.lic";
// Setzen Sie die Lizenz für unser Aspose.Words-Produkt, indem Sie einen Stream für eine gültige Lizenzdatei in unserem lokalen Dateisystem übergeben.
{
    System::SharedPtr<System::IO::Stream> myStream = System::IO::File::OpenRead(System::IO::Path::Combine(get_LicenseDir(), testLicenseFileName));
    auto license = System::MakeObject<Aspose::Words::License>();
    license->SetLicense(myStream);
}
```

## Siehe auch

* Class [License](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## License::SetLicense(const System::String\&) method


Lizenziert die Komponente.

```cpp
void Aspose::Words::License::SetLicense(const System::String &licenseName)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| licenseName | const System::String\& | Kann ein voller oder kurzer Dateiname sein. Verwenden Sie eine leere Zeichenkette, um in den Evaluierungsmodus zu wechseln. |
## Hinweise


Versucht, die Lizenz an den folgenden Orten zu finden:

1. Expliziter Pfad.
1. Der Ordner, der die Aspose.Words-Bibliothek enthält.
1. Der Ordner, der die Anwendung des Kunden enthält.



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
## License::SetLicense(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::License::SetLicense(std::basic_istream<CharType, Traits> &stream)
```

## Siehe auch

* Class [License](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
