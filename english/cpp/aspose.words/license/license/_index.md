---
title: Aspose::Words::License::License constructor
linktitle: License
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::License::License constructor. Initializes a new instance of this class in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words/license/license/
---
## License::License constructor


Initializes a new instance of this class.

```cpp
Aspose::Words::License::License()
```


## Examples



Shows how to initialize a license for Aspose.Words using a license file in the local file system. 
```cpp
System::String testLicenseFileName = u"Aspose.Total.C++.lic";

// Set the license for our Aspose.Words product by passing the local file system filename of a valid license file.
System::String licenseFileName = System::IO::Path::Combine(get_LicenseDir(), testLicenseFileName);

auto license = System::MakeObject<Aspose::Words::License>();
license->SetLicense(licenseFileName);

// Create a copy of our license file in the binaries folder of our application.
System::String licenseCopyFileName = System::IO::Path::Combine(get_AssemblyDir(), testLicenseFileName);
System::IO::File::Copy(licenseFileName, licenseCopyFileName);

// If we pass a file's name without a path,
// the SetLicense will search several local file system locations for this file.
// One of those locations will be the "bin" folder, which contains a copy of our license file.
license->SetLicense(testLicenseFileName);
```

## See Also

* Class [License](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
