---
title: License Class
linktitle: License
articleTitle: License
second_title: Aspose.Words for .NET
description: Aspose.Words.License class. Provides methods to license the component in C#.
type: docs
weight: 3360
url: /net/aspose.words/license/
---
## License class

Provides methods to license the component.

To learn more, visit the [Licensing and Subscription](https://docs.aspose.com/words/net/licensing/) documentation article.

```csharp
public class License
```

## Constructors

| Name | Description |
| --- | --- |
| [License](license/)() | Initializes a new instance of this class. |

## Methods

| Name | Description |
| --- | --- |
| [SetLicense](../../aspose.words/license/setlicense/#setlicense)(*Stream*) | Licenses the component. |
| [SetLicense](../../aspose.words/license/setlicense/#setlicense_1)(*string*) | Licenses the component. |

## Examples

Shows how initialize a license for Aspose.Words using a license file in the local file system.

```csharp
// Set the license for our Aspose.Words product by passing the local file system filename of a valid license file.
string licenseFileName = Path.Combine(LicenseDir, "Aspose.Words.NET.lic");

License license = new License();
license.SetLicense(licenseFileName);

// Create a copy of our license file in the binaries folder of our application.
string licenseCopyFileName = Path.Combine(AssemblyDir, "Aspose.Words.NET.lic");
File.Copy(licenseFileName, licenseCopyFileName);

// If we pass a file's name without a path,
// the SetLicense will search several local file system locations for this file.
// One of those locations will be the "bin" folder, which contains a copy of our license file.
license.SetLicense("Aspose.Words.NET.lic");
```

### See Also

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
