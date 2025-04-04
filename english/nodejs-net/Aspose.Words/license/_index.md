---
title: License class
linktitle: License class
articleTitle: License class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.License class. Provides methods to license the component"
type: docs
weight: 740
url: /nodejs-net/aspose.words/license/
---

## License class

Provides methods to license the component.
To learn more, visit the [Licensing and Subscription](https://docs.aspose.com/words/nodejs-net/licensing/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [License()](./constructor/#default) | Initializes a new instance of this class. |

### Methods

| Name | Description |
| --- | --- |
|[ setLicense(licenseName)](./setLicense/#string) | Licenses the component. |
|[ setLicense(stream)](./setLicense/#buffer) | Licenses the component. |

### Examples

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

### See Also

* module [Aspose.Words](../)

