---
title: Aspose::Words::ImportFormatOptions::get_KeepSourceNumbering method
linktitle: get_KeepSourceNumbering
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ImportFormatOptions::get_KeepSourceNumbering method. Gets or sets a boolean value that specifies how the numbering will be imported when it clashes in source and destination documents. The default value is false in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words/importformatoptions/get_keepsourcenumbering/
---
## ImportFormatOptions::get_KeepSourceNumbering method


Gets or sets a boolean value that specifies how the numbering will be imported when it clashes in source and destination documents. The default value is **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_KeepSourceNumbering() const
```


## Examples



Shows how to import a document with numbered lists. 
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List source.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List destination.docx");

ASSERT_EQ(4, dstDoc->get_Lists()->get_Count());

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();

// If there is a clash of list styles, apply the list format of the source document.
// Set the "KeepSourceNumbering" property to "false" to not import any list numbers into the destination document.
// Set the "KeepSourceNumbering" property to "true" import all clashing
// list style numbering with the same appearance that it had in the source document.
options->set_KeepSourceNumbering(isKeepSourceNumbering);

dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);
dstDoc->UpdateListLabels();

ASSERT_EQ(isKeepSourceNumbering ? 5 : 4, dstDoc->get_Lists()->get_Count());
```


Shows how resolve a clash when importing documents that have lists with the same list definition identifier. 
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List with the same definition identifier - source.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List with the same definition identifier - destination.docx");

// Set the "KeepSourceNumbering" property to "true" to apply a different list definition ID
// to identical styles as Aspose.Words imports them into destination documents.
auto importFormatOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importFormatOptions->set_KeepSourceNumbering(true);

dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::UseDestinationStyles, importFormatOptions);
dstDoc->UpdateListLabels();
```


Shows how to resolve list numbering clashes in source and destination documents. 
```cpp
// Open a document with a custom list numbering scheme, and then clone it.
// Since both have the same numbering format, the formats will clash if we import one document into the other.
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom list numbering.docx");
System::SharedPtr<Aspose::Words::Document> dstDoc = srcDoc->Clone();

// When we import the document's clone into the original and then append it,
// then the two lists with the same list format will join.
// If we set the "KeepSourceNumbering" flag to "false", then the list from the document clone
// that we append to the original will carry on the numbering of the list we append it to.
// This will effectively merge the two lists into one.
// If we set the "KeepSourceNumbering" flag to "true", then the document clone
// list will preserve its original numbering, making the two lists appear as separate lists.
auto importFormatOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importFormatOptions->set_KeepSourceNumbering(keepSourceNumbering);

auto importer = System::MakeObject<Aspose::Words::NodeImporter>(srcDoc, dstDoc, Aspose::Words::ImportFormatMode::KeepDifferentStyles, importFormatOptions);
for (auto&& paragraph : System::IterateOver<Aspose::Words::Paragraph>(srcDoc->get_FirstSection()->get_Body()->get_Paragraphs()))
{
    System::SharedPtr<Aspose::Words::Node> importedNode = importer->ImportNode(paragraph, true);
    dstDoc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Node>>(importedNode);
}

dstDoc->UpdateListLabels();

if (keepSourceNumbering)
{
    ASSERT_EQ(System::String(u"6. Item 1\r\n") + u"7. Item 2 \r\n" + u"8. Item 3\r\n" + u"9. Item 4\r\n" + u"6. Item 1\r\n" + u"7. Item 2 \r\n" + u"8. Item 3\r\n" + u"9. Item 4", dstDoc->get_FirstSection()->get_Body()->ToString(Aspose::Words::SaveFormat::Text).Trim());
}
else
{
    ASSERT_EQ(System::String(u"6. Item 1\r\n") + u"7. Item 2 \r\n" + u"8. Item 3\r\n" + u"9. Item 4\r\n" + u"10. Item 1\r\n" + u"11. Item 2 \r\n" + u"12. Item 3\r\n" + u"13. Item 4", dstDoc->get_FirstSection()->get_Body()->ToString(Aspose::Words::SaveFormat::Text).Trim());
}
```

## See Also

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
