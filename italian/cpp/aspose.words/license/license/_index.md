---
title: "Costruttore Aspose::Words::License::License"
linktitle: "License"
second_title: "Riferimento API Aspose.Words per C++"
description: "Costruttore Aspose::Words::License::License. Inizializza una nuova istanza di questa classe in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words/license/license/
---
## License::License constructor


Inizializza una nuova istanza di questa classe.

```cpp
Aspose::Words::License::License()
```


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

* Class [License](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
