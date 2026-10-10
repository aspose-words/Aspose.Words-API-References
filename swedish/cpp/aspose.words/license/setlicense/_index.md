---
title: "Aspose::Words::License::SetLicense metod"
linktitle: "SetLicense"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::License::SetLicense metod. Licensierar komponenten i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words/license/setlicense/
---
## License::SetLicense(const System::SharedPtr\<System::IO::Stream\>\&) method


Licensierar komponenten.

```cpp
void Aspose::Words::License::SetLicense(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| ström | const System::SharedPtr\<System::IO::Stream\>\& | En ström som innehåller licensen. |
## Anmärkningar


Använd den här metoden för att läsa in en licens från en ström.

## Exempel



Visar hur man initierar en licens för Aspose.Words från en ström.
```cpp
System::String testLicenseFileName = u"Aspose.Words.Cpp.lic";
// Ställ in licensen för vår Aspose.Words-produkt genom att skicka en ström för en giltig licensfil i vårt lokala filsystem.
{
    System::SharedPtr<System::IO::Stream> myStream = System::IO::File::OpenRead(System::IO::Path::Combine(get_LicenseDir(), testLicenseFileName));
    auto license = System::MakeObject<Aspose::Words::License>();
    license->SetLicense(myStream);
}
```

## Se även

* Class [License](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## License::SetLicense(const System::String\&) method


Licensierar komponenten.

```cpp
void Aspose::Words::License::SetLicense(const System::String &licenseName)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| licenseName | const System::String\& | Kan vara ett fullständigt eller kort filnamn. Använd en tom sträng för att växla till utvärderingsläge. |
## Anmärkningar


Försöker hitta licensen på följande platser:

1. Explicit sökväg.
1. Mappen som innehåller Aspose.Words‑biblioteket.
1. Mappen som innehåller klientens applikation.



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
## License::SetLicense(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::License::SetLicense(std::basic_istream<CharType, Traits> &stream)
```

## Se även

* Class [License](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
