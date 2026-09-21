---
title: "Aspose::Words::License class"
linktitle: "License"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::License class. Tillhandahåller metoder för att licensiera komponenten. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 39000
url: /sv/cpp/aspose.words/license/
---
## License class


Tillhandahåller metoder för att licensiera komponenten. För att lära dig mer, besök dokumentationsartikeln [Licensing and Subscription](https://docs.aspose.com/words/cpp/licensing/) i dokumentationen.

```cpp
class License : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [License](./license/)() | Initierar en ny instans av den här klassen. |
| [SetLicense](./setlicense/)(const System::String\&) | Licensierar komponenten. |
| [SetLicense](./setlicense/)(const System::SharedPtr\<System::IO::Stream\>\&) | Licensierar komponenten. |
| [SetLicense](./setlicense/)(std::basic_istream\<CharType, Traits\>\&) |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
