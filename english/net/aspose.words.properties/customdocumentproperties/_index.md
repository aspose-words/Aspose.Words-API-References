---
title: CustomDocumentProperties Class
linktitle: CustomDocumentProperties
articleTitle: CustomDocumentProperties
second_title: Aspose.Words for .NET
description: Aspose.Words.Properties.CustomDocumentProperties class. A collection of custom document properties in C#.
type: docs
weight: 4370
url: /net/aspose.words.properties/customdocumentproperties/
---
## CustomDocumentProperties class

A collection of custom document properties.

To learn more, visit the [Work with Document Properties](https://docs.aspose.com/words/net/work-with-document-properties/) documentation article.

```csharp
public class CustomDocumentProperties : DocumentPropertyCollection
```

## Properties

| Name | Description |
| --- | --- |
| [Count](../../aspose.words.properties/documentpropertycollection/count/) { get; } | Gets number of items in the collection. |
| [Item](../../aspose.words.properties/documentpropertycollection/item/) { get; } | Returns a [`DocumentProperty`](../documentproperty/) object by index. |
| virtual [Item](../../aspose.words.properties/documentpropertycollection/item/) { get; } | Returns a [`DocumentProperty`](../documentproperty/) object by the name of the property. |

## Methods

| Name | Description |
| --- | --- |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add)(*string, bool*) | Creates a new custom document property of the Boolean data type. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_3)(*string, DateTime*) | Creates a new custom document property of the DateTime data type. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_1)(*string, double*) | Creates a new custom document property of the Double data type. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_2)(*string, int*) | Creates a new custom document property of the Number data type. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_4)(*string, string*) | Creates a new custom document property of the String data type. |
| [AddLinkToContent](../../aspose.words.properties/customdocumentproperties/addlinktocontent/)(*string, string*) | Creates a new linked to content custom document property. |
| [Clear](../../aspose.words.properties/documentpropertycollection/clear/)() | Removes all properties from the collection. |
| [Contains](../../aspose.words.properties/documentpropertycollection/contains/)(*string*) | Returns `true` if a property with the specified name exists in the collection. |
| [GetEnumerator](../../aspose.words.properties/documentpropertycollection/getenumerator/)() | Returns an enumerator object that can be used to iterate over all items in the collection. |
| [IndexOf](../../aspose.words.properties/documentpropertycollection/indexof/)(*string*) | Gets the index of a property by name. |
| [Remove](../../aspose.words.properties/documentpropertycollection/remove/)(*string*) | Removes a property with the specified name from the collection. |
| [RemoveAt](../../aspose.words.properties/documentpropertycollection/removeat/)(*int*) | Removes a property at the specified index. |

## Remarks

Each [`DocumentProperty`](../documentproperty/) object represents a custom property of a container document.

The names of the properties are case-insensitive.

The properties in the collection are sorted alphabetically by name.

## Examples

Shows how to work with custom document properties.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// Every document contains a collection of custom properties, which, like the built-in properties, are key-value pairs.
// The document has a fixed list of built-in properties. The user creates all of the custom properties. 
Assert.AreEqual("Value of custom document property", doc.CustomDocumentProperties["CustomProperty"].ToString());

doc.CustomDocumentProperties.Add("CustomProperty2", "Value of custom document property #2");

Console.WriteLine("Custom Properties:");
foreach (var customDocumentProperty in doc.CustomDocumentProperties)
{
    Console.WriteLine(customDocumentProperty.Name);
    Console.WriteLine($"\tType:\t{customDocumentProperty.Type}");
    Console.WriteLine($"\tValue:\t\"{customDocumentProperty.Value}\"");
}
```

### See Also

* class [Document](../../aspose.words/document/)
* property [BuiltInDocumentProperties](../../aspose.words/document/builtindocumentproperties/)
* property [CustomDocumentProperties](../../aspose.words/document/customdocumentproperties/)
* class [DocumentPropertyCollection](../documentpropertycollection/)
* namespace [Aspose.Words.Properties](../../aspose.words.properties/)
* assembly [Aspose.Words](../../)
