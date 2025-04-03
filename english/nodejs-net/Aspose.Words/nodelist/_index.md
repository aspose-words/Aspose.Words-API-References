---
title: NodeList class
linktitle: NodeList class
articleTitle: NodeList class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.NodeList class. Represents a collection of nodes matching an XPath query executed using the [CompositeNode.selectNodes()](../compositenode/selectNodes/#string) method"
type: docs
weight: 880
url: /nodejs-net/aspose.words/nodelist/
---

## NodeList class

Represents a collection of nodes matching an XPath query executed using the [CompositeNode.selectNodes()](../compositenode/selectNodes/#string) method.
To learn more, visit the [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/nodejs-net/aspose-words-document-object-model/) documentation article.




### Remarks

[NodeList](./) is returned by [CompositeNode.selectNodes()](../compositenode/selectNodes/#string) and contains a collection
of nodes matching the XPath query.

[NodeList](./) supports indexed access and iteration.

> **NOTE**
>
> Treat the [NodeList](./) collection as a "snapshot" collection. [NodeList](./) starts
> as a "live" collection because the nodes are not actually retrieved when the XPath query is run.
> The nodes are only retrieved upon access and at this time the node and all nodes that precede
> it are cached forming a "snapshot" collection.




### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets the number of nodes in the list. |
| [this[]](./this[]/) |  |

### Methods

| Name | Description |
| --- | --- |
|[ toArray()](./toArray/#default) | Copies all nodes from the collection to a new array of nodes. |

### Examples

Shows how to find all hyperlinks in a Word document, and then change their URLs and display names.

```js
describe("ExReplaceHyperlinks", () => {
  test('Fields', () => {
    let doc = new aw.Document(base.myDir + "Hyperlinks.docx");

    // Hyperlinks in a Word documents are fields. To begin looking for hyperlinks, we must first find all the fields.
    // Use the "SelectNodes" method to find all the fields in the document via an XPath.
    let fieldStarts = doc.selectNodes("//FieldStart");

    foreach (FieldStart fieldStart in fieldStarts.OfType<FieldStart>())
    {
      if (fieldStart.fieldType == aw.Fields.FieldType.FieldHyperlink)
      {
        let hyperlink = new aw.RW.OfficeShared.Hyperlink(fieldStart);

        // Hyperlinks that link to bookmarks do not have URLs.
        if (hyperlink.IsLocal)
          continue;

        // Give each URL hyperlink a new URL and name.
        hyperlink.target = NewUrl;
        hyperlink.name = NewName;
      }
    }

    doc.save(base.artifactsDir + "ReplaceHyperlinks.fields.docx");
  });


  private const string NewUrl = @"http://www.aspose.com";
  private const string NewName = "Aspose - The .NET & Java Component Publisher";

  /// <summary>
  /// HYPERLINK fields contain and display hyperlinks in the document body. A field in Aspose.Words 
  /// consists of several nodes, and it might be difficult to work with all those nodes directly. 
  /// This implementation will work only if the hyperlink code and name each consist of only one Run node.
  ///
  /// The node structure for fields is as follows:
  /// 
  /// [FieldStart][Run - field code][FieldSeparator][Run - field result][FieldEnd]
  /// 
  /// Below are two example field codes of HYPERLINK fields:
  /// HYPERLINK "url"
  /// HYPERLINK \l "bookmark name"
  /// 
  /// A field's "Result" property contains text that the field displays in the document body to the user.
  /// </summary>
  internal class Hyperlink
  internal Hyperlink(FieldStart fieldStart)
  {
    if (fieldStart == null)
      throw new ArgumentNullException("fieldStart");
    if (fieldStart.fieldType != aw.Fields.FieldType.FieldHyperlink)
      throw new ArgumentException("Field start type must be FieldHyperlink.");

    mFieldStart = fieldStart;

      // Find the field separator node.
    mFieldSeparator = FindNextSibling(mFieldStart, aw.NodeType.FieldSeparator);
    if (mFieldSeparator == null)
      throw new InvalidOperationException("Cannot find field separator.");

      // Normally, we can always find the field's end node, but the example document 
      // contains a paragraph break inside a hyperlink, which puts the field end 
      // in the next paragraph. It will be much more complicated to handle fields which span several 
      // paragraphs correctly. In this case allowing field end to be null is enough.
    mFieldEnd = FindNextSibling(mFieldSeparator, aw.NodeType.FieldEnd);

      // Field code looks something like "HYPERLINK "http:\\www.myurl.com"", but it can consist of several runs.
    string fieldCode = GetTextSameParent(mFieldStart.nextSibling, mFieldSeparator);
    Match match = gRegex.match(fieldCode.trim());

      // The hyperlink is local if \l is present in the field code.
    mIsLocal = match.groups.at(1).length > 0; 
    mTarget = match.groups.at(2).value;
  }

    /// <summary>
    /// Gets or sets the display name of the hyperlink.
    /// </summary>
  internal string Name
  {
    get
    {
      return GetTextSameParent(mFieldSeparator, mFieldEnd);
    }
    set
    {
        // Hyperlink display name is stored in the field result, which is a Run 
        // node between field separator and field end.
      let fieldResult = (Run) mFieldSeparator.nextSibling;
      fieldResult.text = value;

        // If the field result consists of more than one run, delete these runs.
      RemoveSameParent(fieldResult.nextSibling, mFieldEnd);
    }
  }

    /// <summary>
    /// Gets or sets the target URL or bookmark name of the hyperlink.
    /// </summary>
  internal string Target
  {
    get
    {
      return mTarget;
    }
    set
    {
      mTarget = value;
      UpdateFieldCode();
    }
  }

    /// <summary>
    /// True if the hyperlinks target is a bookmark inside the document. False if the hyperlink is a URL.
    /// </summary>
  internal bool IsLocal
  {
    get
    {
      return mIsLocal;
    }
    set
    {
      mIsLocal = value;
      UpdateFieldCode();
    }
  }

  private void UpdateFieldCode()
  {
      // A field's field code is in a Run node between the field's start node and field separator.
    let fieldCode = (Run) mFieldStart.nextSibling;
    fieldCode.text = string.format("HYPERLINK {0}\"{1}\"", ((mIsLocal) ? "\\l " : ""), mTarget);

      // If the field code consists of more than one run, delete these runs.
    RemoveSameParent(fieldCode.nextSibling, mFieldSeparator);
  }

    /// <summary>
    /// Goes through siblings starting from the start node until it finds a node of the specified type or null.
    /// </summary>
  private static Node FindNextSibling(Node startNode, NodeType nodeType)
  {
    for (let node = startNode; node != null; node = node.nextSibling)
    {
      if (node.nodeType == nodeType)
        return node;
    }

    return null;
  }

    /// <summary>
    /// Retrieves text from start up to but not including the end node.
    /// </summary>
  private static string GetTextSameParent(Node startNode, Node endNode)
  {
    if ((endNode != null) && (startNode.parentNode != endNode.parentNode))
      throw new ArgumentException("Start and end nodes are expected to have the same parent.");

    let builder = new StringBuilder();
    for (let child = startNode; !child.equals(endNode); child = child.nextSibling)
      builder.append(child.getText());

    return builder.toString();
  }

    /// <summary>
    /// Removes nodes from start up to but not including the end node.
    /// Assumes that the start and end nodes have the same parent.
    /// </summary>
  private static void RemoveSameParent(Node startNode, Node endNode)
  {
    if (endNode != null && startNode.parentNode != endNode.parentNode)
      throw new ArgumentException("Start and end nodes are expected to have the same parent.");

    let curChild = startNode;
    while ((curChild != null) && (curChild != endNode))
    {
      let nextChild = curChild.nextSibling;
      curChild.remove();
      curChild = nextChild;
    }
  }

  private readonly Node mFieldStart;
  private readonly Node mFieldSeparator;
  private readonly Node mFieldEnd;
  private bool mIsLocal;
  private string mTarget;

  private static readonly Regex gRegex = new Regex(
    "\\S+" + // One or more non spaces HYPERLINK or other word in other languages.
    "\\s+" + // One or more spaces.
    "(?:\"\"\\s+)?" + // Non-capturing optional "" and one or more spaces.
    "(\\\\l\\s+)?" + // Optional \l flag followed by one or more spaces.
    "\"" + // One apostrophe.	
    "([^\"]+)" + // One or more characters, excluding the apostrophe (hyperlink target).
    "\"" // One closing apostrophe.
  );
```

### See Also

* module [Aspose.Words](../)

