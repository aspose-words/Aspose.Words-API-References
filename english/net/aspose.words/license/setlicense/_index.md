---
title: License.SetLicense
linktitle: SetLicense
articleTitle: SetLicense
second_title: Aspose.Words for .NET
description: Effortlessly license your components with our SetLicense method. Unlock full functionality and enhance your project's potential today!
type: docs
weight: 20
url: /net/aspose.words/license/setlicense/
---
## SetLicense(*string*) {#setlicense_1}

Licenses the component.

```csharp
public void SetLicense(string licenseName)
```

| Parameter | Type | Description |
| --- | --- | --- |
| licenseName | String | Can be a full or short file name or name of an embedded resource. Use an empty string to switch to evaluation mode. |

## Remarks

Tries to find the license in the following locations:

1. Explicit path.

2. The folder that contains the Aspose component assembly.

3. The folder that contains the client's calling assembly.

4. The folder that contains the entry (startup) assembly.

5. An embedded resource in the client's calling assembly.

**Note:**On the .NET Compact Framework, tries to find the license only in these locations:

1. Explicit path.

2. An embedded resource in the client's calling assembly.

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

---

## SetLicense(*Stream*) {#setlicense}

Licenses the component.

```csharp
public void SetLicense(Stream stream)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | Stream | A stream that contains the license. |

## Remarks

Use this method to load a license from a stream.

## Examples

Shows how to initialize a license for Aspose.Words from a stream.

```csharp
#if CPLUSPLUS
            string testLicenseFileName = "Aspose.Total.C++.lic";
#else
            string testLicenseFileName = "Aspose.Total.NET.lic";
#endif
            // Set the license for our Aspose.Words product by passing a stream for a valid license file in our local file system.
            using (Stream myStream = File.OpenRead(Path.Combine(LicenseDir, testLicenseFileName)))
            {
                License license = new License();
                license.SetLicense(myStream);
            }
```

### See Also

* class [License](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
