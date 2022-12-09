---
title: License
second_title: Aspose.Words for C++ API Reference
description: Initializes a new instance of this class.
type: docs
weight: 14
url: /cpp/aspose.words/license/license/
---
## License::License constructor


Initializes a new instance of this class.

```cpp
Aspose::Words::License::License()
```


## Examples



Shows how initialize a license for Aspose.Words using a license file in the local file system. 
```cpp
// Set the license for our Aspose.Words product by passing the local file system filename of a valid license file.
String licenseFileName = System::IO::Path::Combine(LicenseDir, u"Aspose.Words.Cpp.lic");

auto license = MakeObject<License>();
license->SetLicense(licenseFileName);

// Create a copy of our license file in the binaries folder of our application.
String licenseCopyFileName = System::IO::Path::Combine(AssemblyDir, u"Aspose.Words.Cpp.lic");
System::IO::File::Copy(licenseFileName, licenseCopyFileName);

// If we pass a file's name without a path,
// the SetLicense will search several local file system locations for this file.
// One of those locations will be the "bin" folder, which contains a copy of our license file.
license->SetLicense(u"Aspose.Words.Cpp.lic");
```

## See Also

* Class [License](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
