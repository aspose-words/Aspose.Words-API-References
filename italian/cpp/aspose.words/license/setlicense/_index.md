---
title: "Metodo SetLicense di Aspose::Words::License"
linktitle: "SetLicense"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo SetLicense di Aspose::Words::License. Attiva la licenza del componente in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words/license/setlicense/
---
## License::SetLicense(const System::SharedPtr\<System::IO::Stream\>\&) method


Licenzia il componente.

```cpp
void Aspose::Words::License::SetLicense(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| flusso | const System::SharedPtr\<System::IO::Stream\>\& | Uno stream che contiene la licenza. |
## Note


Utilizza questo metodo per caricare una licenza da uno stream.

## Esempi



Mostra come inizializzare una licenza per Aspose.Words da uno stream.
```cpp
System::String testLicenseFileName = u"Aspose.Words.Cpp.lic";
// Imposta la licenza per il nostro prodotto Aspose.Words passando uno stream per un file di licenza valido nel nostro file system locale.
{
    System::SharedPtr<System::IO::Stream> myStream = System::IO::File::OpenRead(System::IO::Path::Combine(get_LicenseDir(), testLicenseFileName));
    auto license = System::MakeObject<Aspose::Words::License>();
    license->SetLicense(myStream);
}
```

## Vedi anche

* Class [License](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## License::SetLicense(const System::String\&) method


Licenzia il componente.

```cpp
void Aspose::Words::License::SetLicense(const System::String &licenseName)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| licenseName | const System::String\& | Può essere un nome file completo o breve. Usa una stringa vuota per passare alla modalità di valutazione. |
## Note


Cerca di trovare la licenza nelle seguenti posizioni:

1. Percorso esplicito.
1. La cartella che contiene la libreria Aspose.Words.
1. La cartella che contiene l'applicazione del cliente.



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
## License::SetLicense(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::License::SetLicense(std::basic_istream<CharType, Traits> &stream)
```

## Vedi anche

* Class [License](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
