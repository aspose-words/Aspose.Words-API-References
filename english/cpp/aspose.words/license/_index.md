---
title: Aspose::Words::License class
linktitle: License
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::License class. Provides methods to license the component. To learn more, visit the  documentation article in C++.'
type: docs
weight: 39000
url: /cpp/aspose.words/license/
---
## License class


Provides methods to license the component. To learn more, visit the [Licensing and Subscription](https://docs.aspose.com/words/cpp/licensing/) documentation article.

```cpp
class License : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [License](./license/)() | Initializes a new instance of this class. |
| [SetLicense](./setlicense/)(const System::String\&) | Licenses the component. |
| [SetLicense](./setlicense/)(const System::SharedPtr\<System::IO::Stream\>\&) | Licenses the component. |
| [SetLicense](./setlicense/)(std::basic_istream\<CharType, Traits\>\&) |  |
| static [Type](./type/)() |  |

## Examples



Shows how to initialize a license for Aspose.Words using a license file in the local file system. 
```cpp
System::String testLicenseFileName = u"Aspose.Words.Cpp.lic";

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
