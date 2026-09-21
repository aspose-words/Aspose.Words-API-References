---
title: "Aspose::Words::License::License konstruktor"
linktitle: "License"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::License::License konstruktor. Initierar en ny instans av denna klass i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words/license/license/
---
## License::License constructor


Initierar en ny instans av den här klassen.

```cpp
Aspose::Words::License::License()
```


## Exempel



Visar hur man initierar en licens för Aspose.Words med en licensfil i det lokala filsystemet.
```cpp
System::String testLicenseFileName = u"Aspose.Words.Cpp.lic";

// Ställ in licensen för vår Aspose.Words-produkt genom att ange filnamnet i det lokala filsystemet för en giltig licensfil.
System::String licenseFileName = System::IO::Path::Combine(get_LicenseDir(), testLicenseFileName);

auto license = System::MakeObject<Aspose::Words::License>();
license->SetLicense(licenseFileName);

// Skapa en kopia av vår licensfil i binärkatalogen för vår applikation.
System::String licenseCopyFileName = System::IO::Path::Combine(get_AssemblyDir(), testLicenseFileName);
System::IO::File::Copy(licenseFileName, licenseCopyFileName);

// Om vi anger ett filnamn utan en sökväg,
// kommer SetLicense att söka på flera lokala filsystemplatser efter den här filen.
// En av dessa platser kommer att vara "bin"-mappen, som innehåller en kopia av vår licensfil.
license->SetLicense(testLicenseFileName);
```

## Se även

* Class [License](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
