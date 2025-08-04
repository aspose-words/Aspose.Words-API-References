---
title: License
linktitle: License
articleTitle: License
second_title: Aspose.Words for .NET
description: Effortlessly create and manage licenses with our constructor class. Simplify your licensing process and enhance efficiency today!
type: docs
weight: 10
url: /net/aspose.words/license/license/
---
## License constructor

Initializes a new instance of this class.

```csharp
public License()
```

## Examples

Shows how to initialize a license for Aspose.Words using a license file in the local file system.

```csharp
#if CPLUSPLUS
            string testLicenseFileName = "Aspose.Total.C++.lic";
#else
            string testLicenseFileName = "Aspose.Total.NET.lic";
#endif

            // Set the license for our Aspose.Words product by passing the local file system filename of a valid license file.
            string licenseFileName = Path.Combine(LicenseDir, testLicenseFileName);

            License license = new License();
            license.SetLicense(licenseFileName);

            // Create a copy of our license file in the binaries folder of our application.
            string licenseCopyFileName = Path.Combine(AssemblyDir, testLicenseFileName);
            File.Copy(licenseFileName, licenseCopyFileName);

            // If we pass a file's name without a path,
            // the SetLicense will search several local file system locations for this file.
            // One of those locations will be the "bin" folder, which contains a copy of our license file.
            license.SetLicense(testLicenseFileName);
```

### See Also

* class [License](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
