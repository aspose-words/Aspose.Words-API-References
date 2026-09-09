---
title: SignOptions.timestampSettings property
linktitle: timestampSettings property
articleTitle: timestampSettings property
second_title: Aspose.Words for Node.js
description: "SignOptions.timestampSettings property. Specifies settings for timestamping the digital signature using an RFC 3161 timestamp authority (TSA)"
type: docs
weight: 120
url: /nodejs-net/aspose.words.digitalsignatures/signoptions/timestampSettings/
---

## SignOptions.timestampSettings property

Specifies settings for timestamping the digital signature using an RFC 3161 timestamp authority (TSA).
The default value is ``null`` and the digital signature will not be time-stamped.



```js
get timestampSettings(): Aspose.Words.DigitalSignatures.DigitalSignatureTimestampSettings
```

### Remarks

When this property is set to a valid [DigitalSignatureTimestampSettings](../../digitalsignaturetimestampsettings/) object,
and [SignOptions.xmlDsigLevel](../xmlDsigLevel/) is set to [XmlDsigLevel.XAdEsT](../../xmldsiglevel/#XAdEsT) or higher,
the digital signature will be time-stamped.



### See Also

* module [Aspose.Words.DigitalSignatures](../../)
* class [SignOptions](../)

