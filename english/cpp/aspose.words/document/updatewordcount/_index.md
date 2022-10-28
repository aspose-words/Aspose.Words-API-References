---
title: UpdateWordCount
second_title: Aspose.Words for C++ API Reference
description: Updates word count properties of the document.
type: docs
weight: 1210
url: /cpp/aspose.words/document/updatewordcount/
---
## Document.UpdateWordCount() method


Updates word count properties of the document.

```cpp
void Aspose::Words::Document::UpdateWordCount()
```


**UpdateWordCount** recalculates and updates Characters, [Words](../../) and Paragraphs properties in the [BuiltInDocumentProperties](../get_builtindocumentproperties/) collection of the **Document**.

Note that **UpdateWordCount** does not update number of lines and pages properties. Use the [UpdateWordCount](./) overload and pass True value as a parameter to do that.

When you use an evaluation version, the evaluation watermark will also be included in the word count.

## Examples




Shows how to update all list labels in a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") +
                 u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder->Write(String(u"Ut enim ad minim veniam, ") + u"quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words does not track document metrics like these in real time.
ASSERT_EQ(0, doc->get_BuiltInDocumentProperties()->get_Characters());
ASSERT_EQ(0, doc->get_BuiltInDocumentProperties()->get_Words());
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Paragraphs());
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Lines());

// To get accurate values for three of these properties, we will need to update them manually.
doc->UpdateWordCount();

ASSERT_EQ(196, doc->get_BuiltInDocumentProperties()->get_Characters());
ASSERT_EQ(36, doc->get_BuiltInDocumentProperties()->get_Words());
ASSERT_EQ(2, doc->get_BuiltInDocumentProperties()->get_Paragraphs());

// For the line count, we will need to call a specific overload of the updating method.
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Lines());

doc->UpdateWordCount(true);

ASSERT_EQ(4, doc->get_BuiltInDocumentProperties()->get_Lines());
```

## Document.UpdateWordCount(bool) method


Updates word count properties of the document, optionally updates [Lines](../../../aspose.words.properties/builtindocumentproperties/get_lines/) property.

```cpp
void Aspose::Words::Document::UpdateWordCount(bool updateLinesCount)
```


| Parameter | Type | Description |
| --- | --- | --- |
| updateLinesCount | bool | True if number of lines in the document shall be calculated. |

## Examples




Shows how to update all list labels in a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") +
                 u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder->Write(String(u"Ut enim ad minim veniam, ") + u"quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words does not track document metrics like these in real time.
ASSERT_EQ(0, doc->get_BuiltInDocumentProperties()->get_Characters());
ASSERT_EQ(0, doc->get_BuiltInDocumentProperties()->get_Words());
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Paragraphs());
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Lines());

// To get accurate values for three of these properties, we will need to update them manually.
doc->UpdateWordCount();

ASSERT_EQ(196, doc->get_BuiltInDocumentProperties()->get_Characters());
ASSERT_EQ(36, doc->get_BuiltInDocumentProperties()->get_Words());
ASSERT_EQ(2, doc->get_BuiltInDocumentProperties()->get_Paragraphs());

// For the line count, we will need to call a specific overload of the updating method.
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Lines());

doc->UpdateWordCount(true);

ASSERT_EQ(4, doc->get_BuiltInDocumentProperties()->get_Lines());
```

