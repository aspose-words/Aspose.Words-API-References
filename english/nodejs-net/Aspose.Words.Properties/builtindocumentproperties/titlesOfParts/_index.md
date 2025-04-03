---
title: BuiltInDocumentProperties.titlesOfParts property
linktitle: titlesOfParts property
articleTitle: titlesOfParts property
second_title: Aspose.Words for NodeJs
description: "BuiltInDocumentProperties.titlesOfParts property. Each string in the array specifies the name of a part in the document."
type: docs
weight: 310
url: /nodejs-net/aspose.words.properties/builtindocumentproperties/titlesOfParts/
---

## BuiltInDocumentProperties.titlesOfParts property

Each string in the array specifies the name of a part in the document.


```js
get titlesOfParts(): string[]
```

### Remarks

Aspose.Words does not update this property.




### Examples

Shows the relationship between "HeadingPairs" and "TitlesOfParts" properties.

```js
let doc = new aw.Document(base.myDir + "Heading pairs and titles of parts.docx");

// We can find the combined values of these collections via
// "File" -> "Properties" -> "Advanced Properties" -> "Contents" tab.
// The HeadingPairs property is a collection of <string, int> pairs that
// determines how many document parts a heading spans across.
let headingPairs = doc.builtInDocumentProperties.headingPairs;

// The TitlesOfParts property contains the names of parts that belong to the above headings.
let titlesOfParts = doc.builtInDocumentProperties.titlesOfParts;

let headingPairsIndex = 0;
let titlesOfPartsIndex = 0;
/*while (headingPairsIndex < headingPairs.length)
{
  console.log(`Parts for ${headingPairs.at(headingPairsIndex++)}:`);
  let partsCount = headingPairs.at(headingPairsIndex++);

  for (let i = 0; i < partsCount; i++)
    console.log(`\t\"${titlesOfParts.at(titlesOfPartsIndex++)}\"`);
}*/
```

### See Also

* module [Aspose.Words.Properties](../../)
* class [BuiltInDocumentProperties](../)

