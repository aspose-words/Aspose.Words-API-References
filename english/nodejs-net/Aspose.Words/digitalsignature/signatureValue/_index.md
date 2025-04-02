---
title: DigitalSignature.signatureValue property
linktitle: signatureValue property
articleTitle: signatureValue property
second_title: Aspose.Words for NodeJs
description: "DigitalSignature.signatureValue property. Gets an array of bytes representing a signature value."
type: docs
weight: 70
url: /nodejs-net/Aspose.Words/digitalsignature/signatureValue/
---

## DigitalSignature.signatureValue property

Gets an array of bytes representing a signature value.


```js
get signatureValue(): number[]
```

### Examples

Shows how to get a digital signature value from a digitally signed document.

```js
const doc = new aw.Document(base.myDir + "Digitally signed.docx");
for (var i = 0; i < doc.digitalSignatures.count; i++) {
  const signature = doc.digitalSignatures.at(i);
  const buffer = Buffer.from(signature.signatureValue);
  const signatureValue = buffer.toString('base64');
  expect(signatureValue).toEqual("K1cVLLg2kbJRAzT5WK+m++G8eEO+l7S+5ENdjMxxTXkFzGUfvwxREuJdSFj9AbD" +
                                 "MhnGvDURv9KEhC25DDF1al8NRVR71TF3CjHVZXpYu7edQS5/yLw/k5CiFZzCp1+MmhOdYPcVO+Fm" +
                                 "+9fKr2iNLeyYB+fgEeZHfTqTFM2WwAqo=");
}
```

### See Also

* module [Aspose.Words](../../)
* class [DigitalSignature](../)

