---
title: SetLicense
second_title: Aspose.Words for C++ API Reference
description: Licenses the component.
type: docs
weight: 53
url: /cpp/aspose.words/license/setlicense/
---
## License::SetLicense(const System::SharedPtr\<System::IO::Stream\>\&) method


Licenses the component.

```cpp
void Aspose::Words::License::SetLicense(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parameter | Type | Description |
| --- | --- | --- |
| stream | const System::SharedPtr\<System::IO::Stream\>\& | A stream that contains the license. |
## Remarks


Use this method to load a license from a stream.

## Examples



Shows how to initialize a license for Aspose.Words from a stream. 
```cpp
// Set the license for our Aspose.Words product by passing a stream for a valid license file in our local file system.
{
    SharedPtr<System::IO::Stream> myStream = System::IO::File::OpenRead(System::IO::Path::Combine(LicenseDir, u"Aspose.Words.Cpp.lic"));
    auto license = MakeObject<License>();
    license->SetLicense(myStream);
}
```

## See Also

* Class [License](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
## License::SetLicense(const System::String\&) method


Licenses the component.

```cpp
void Aspose::Words::License::SetLicense(const System::String &licenseName)
```


| Parameter | Type | Description |
| --- | --- | --- |
| licenseName | const System::String\& | Can be a full or short file name. Use an empty string to switch to evaluation mode. |
## Remarks


Tries to find the license in the following locations:

1. Explicit path.
1. The folder that contains the Aspose.Words library.
1. The folder that contains the client's application.



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
## License::SetLicense(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::License::SetLicense(std::basic_istream<CharType, Traits> &stream)
```

## See Also

* Class [License](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
