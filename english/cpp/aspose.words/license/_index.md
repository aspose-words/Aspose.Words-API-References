---
title: License
second_title: Aspose.Words for C++ API Reference
description: Provides methods to license the component.
type: docs
weight: 495
url: /cpp/aspose.words/license/
---
## License class


Provides methods to license the component.

```cpp
class License : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [License](./license/)() | Initializes a new instance of this class. |
| [SetLicense](./setlicense/)(const System::String\&) | Licenses the component. |
| [SetLicense](./setlicense/)(const System::SharedPtr\<System::IO::Stream\>\&) | Licenses the component. |
| [SetLicense](./setlicense/)(std::basic_istream\<CharType, Traits\>\&) |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words](../../)
