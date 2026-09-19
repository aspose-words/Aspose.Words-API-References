---
title: "Aspose::Words::License class"
linktitle: "License"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::License class. Fornisce metodi per licenziare il componente. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 39000
url: /it/cpp/aspose.words/license/
---
## License class


Fornisce metodi per licenziare il componente. Per saperne di più, visita l'articolo di documentazione [Licensing and Subscription](https://docs.aspose.com/words/cpp/licensing/).

```cpp
class License : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [License](./license/)() | Inizializza una nuova istanza di questa classe. |
| [SetLicense](./setlicense/)(const System::String\&) | Licenzia il componente. |
| [SetLicense](./setlicense/)(const System::SharedPtr\<System::IO::Stream\>\&) | Licenzia il componente. |
| [SetLicense](./setlicense/)(std::basic_istream\<CharType, Traits\>\&) |  |
| static [Type](./type/)() |  |

## Esempi



Mostra come inizializzare una licenza per Aspose.Words utilizzando un file di licenza nel file system locale.
```cpp
System::String testLicenseFileName = u"Aspose.Words.Cpp.lic";

// Imposta la licenza per il nostro prodotto Aspose.Words passando il nome file del file di licenza valido nel file system locale.
System::String licenseFileName = System::IO::Path::Combine(get_LicenseDir(), testLicenseFileName);

auto license = System::MakeObject<Aspose::Words::License>();
license->SetLicense(licenseFileName);

// Crea una copia del nostro file di licenza nella cartella binari della nostra applicazione.
System::String licenseCopyFileName = System::IO::Path::Combine(get_AssemblyDir(), testLicenseFileName);
System::IO::File::Copy(licenseFileName, licenseCopyFileName);

// Se passiamo il nome di un file senza un percorso,
// Il SetLicense cercherà diverse posizioni del file system locale per questo file.
// Una di queste posizioni sarà la cartella "bin", che contiene una copia del nostro file di licenza.
license->SetLicense(testLicenseFileName);
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
