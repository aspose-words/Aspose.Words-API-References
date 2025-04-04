---
title: License.setLicense method
linktitle: setLicense method
articleTitle: setLicense method
second_title: Aspose.Words for Node.js
description: "Aspose.Words.License.setLicense method"
type: docs
weight: 20
url: /nodejs-net/aspose.words/license/setLicense/
---

## setLicense(licenseName) {#string}

Licenses the component.


```js
setLicense(licenseName: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| licenseName | string | Can be a full or short file name or name of an embedded resource. Use an empty string to switch to evaluation mode. |

### Remarks

Tries to find the license in the following locations:

1. Explicit path.

2. The folder that contains the Aspose component assembly.

3. The folder that contains the client's calling assembly.

4. The folder that contains the entry (startup) assembly.

5. An embedded resource in the client's calling assembly.

**Note:** On the .NET Compact Framework, tries to find the license only in these locations:

1. Explicit path.

2. An embedded resource in the client's calling assembly.




## setLicense(stream) {#buffer}

Licenses the component.


```js
setLicense(stream: Buffer)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | Buffer | A stream that contains the license. |

### Remarks

Use this method to load a license from a stream.




## Examples

Shows how initialize a license for Aspose.words using a license file in the local file system.

```js
// Set the license for our Aspose.Words product by passing the local file system filename of a valid license file.
const licFilename = "Aspose.Words.NodeJs.NET.lic";
var licenseFileName =  path.join(base.licenseDir, licFilename);

let license = new aw.License();
try {
  license.setLicense(licenseFileName);

  // Create a copy of our license file in the binaries folder of our application.
  var licenseCopyFileName = path.join(base.codeBaseDir, licFilename);
  fs.copyFileSync(licenseFileName, licenseCopyFileName);

  // If we pass a file's name without a path,
  // the SetLicense will search several local file system locations for this file.
  // One of those locations will be the "bin" folder, which contains a copy of our license file.
  license.setLicense(licFilename);
```

Shows how to initialize a license for Aspose.words from a stream.

```js
// Set the license for our Aspose.words product by passing a stream for a valid license file in our local file system.
let data = base.loadFileToBuffer(path.join(base.licenseDir, "Aspose.Words.NodeJs.NET.lic"));
let license = new aw.License();
license.setLicense(data);
```

## See Also

* module [Aspose.Words](../../)
* class [License](../)

