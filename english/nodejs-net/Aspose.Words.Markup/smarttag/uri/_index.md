---
title: SmartTag.uri property
linktitle: uri property
articleTitle: uri property
second_title: Aspose.Words for NodeJs
description: "SmartTag.uri property. Specifies the namespace URI of the smart tag."
type: docs
weight: 50
url: /nodejs-net/Aspose.Words.Markup/smarttag/uri/
---

## SmartTag.uri property

Specifies the namespace URI of the smart tag.


```js
get uri(): string
```

### Remarks

Cannot be ``None``.

Default is empty string.




### Examples

Shows how to create smart tags.

```js
test('Create', () => {
  let doc = new aw.Document();

  // A smart tag appears in a document with Microsoft Word recognizes a part of its text as some form of data,
  // such as a name, date, or address, and converts it to a hyperlink that displays a purple dotted underline.
  let smartTag = new aw.Markup.SmartTag(doc);

  // Smart tags are composite nodes that contain their recognized text in its entirety.
  // Add contents to this smart tag manually.
  smartTag.appendChild(new aw.Run(doc, "May 29, 2019"));

  // Microsoft Word may recognize the above contents as being a date.
  // Smart tags use the "Element" property to reflect the type of data they contain.
  smartTag.element = "date";

  // Some smart tag types process their contents further into custom XML properties.
  smartTag.properties.add(new aw.Markup.CustomXmlProperty("Day", '', "29"));
  smartTag.properties.add(new aw.Markup.CustomXmlProperty("Month", '', "5"));
  smartTag.properties.add(new aw.Markup.CustomXmlProperty("Year", '', "2019"));

  // Set the smart tag's URI to the default value.
  smartTag.uri = "urn:schemas-microsoft-com:office:smarttags";

  doc.firstSection.body.firstParagraph.appendChild(smartTag);
  doc.firstSection.body.firstParagraph.appendChild(new aw.Run(doc, " is a date. "));

  // Create another smart tag for a stock ticker.
  smartTag = new aw.Markup.SmartTag(doc);
  smartTag.element = "stockticker";
  smartTag.uri = "urn:schemas-microsoft-com:office:smarttags";

  smartTag.appendChild(new aw.Run(doc, "MSFT"));

  doc.firstSection.body.firstParagraph.appendChild(smartTag);
  doc.firstSection.body.firstParagraph.appendChild(new aw.Run(doc, " is a stock ticker."));

  // Print all the smart tags in our document using a document visitor.
  doc.accept(new SmartTagPrinter());

  // Older versions of Microsoft Word support smart tags.
  doc.save(base.artifactsDir + "SmartTag.create.doc");

  // Use the "RemoveSmartTags" method to remove all smart tags from a document.
  expect(doc.getChildNodes(aw.NodeType.SmartTag, true).Count).toEqual(2);

  doc.removeSmartTags();

  expect(doc.getChildNodes(aw.NodeType.SmartTag, true).Count).toEqual(0);
});


  /// <summary>
  /// Prints visited smart tags and their contents.
  /// </summary>
private class SmartTagPrinter : DocumentVisitor
{
    /// <summary>
    /// Called when a SmartTag node is encountered in the document.
    /// </summary>
  public override VisitorAction VisitSmartTagStart(SmartTag smartTag)
  {
    console.log(`Smart tag type: ${smartTag.element}`);
    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Called when the visiting of a SmartTag node is ended.
    /// </summary>
  public override VisitorAction VisitSmartTagEnd(SmartTag smartTag)
  {
    console.log(`\tContents: \"${smartTag.toString(aw.SaveFormat.Text)}\"`);

    if (smartTag.properties.count == 0)
    {
      console.log("\tContains no properties");
    }
    else
    {
      Console.write("\tProperties: ");
      string.at(] properties = new string[smartTag.properties.count);
      int index = 0;

      for (let cxp of smartTag.properties)
        properties.at(index++) = `\"${cxp.name}\" = \"${cxp.value}\"`;

      console.log(string.Join(", ", properties));
    }

    return aw.VisitorAction.Continue;
  }
}
```

### See Also

* module [Aspose.Words.Markup](../../)
* class [SmartTag](../)

