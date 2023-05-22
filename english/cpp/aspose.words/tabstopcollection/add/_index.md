---
title: Aspose::Words::TabStopCollection::Add method
linktitle: Add
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::TabStopCollection::Add method. Adds or replaces a tab stop in the collection in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words/tabstopcollection/add/
---
## TabStopCollection::Add(const System::SharedPtr\<Aspose::Words::TabStop\>\&) method


Adds or replaces a tab stop in the collection.

```cpp
void Aspose::Words::TabStopCollection::Add(const System::SharedPtr<Aspose::Words::TabStop> &tabStop)
```


| Parameter | Type | Description |
| --- | --- | --- |
| tabStop | const System::SharedPtr\<Aspose::Words::TabStop\>\& | A tab stop object to add. |
## Remarks


If a tab stop already exists at the specified position, it is replaced.

## Examples



Shows how to add custom tab stops to a document. 
```cpp
auto doc = MakeObject<Document>();
auto paragraph = System::ExplicitCast<Paragraph>(doc->GetChild(NodeType::Paragraph, 0, true));

// Below are two ways of adding tab stops to a paragraph's collection of tab stops via the "ParagraphFormat" property.
// 1 -  Create a "TabStop" object, and then add it to the collection:
auto tabStop = MakeObject<TabStop>(ConvertUtil::InchToPoint(3), TabAlignment::Left, TabLeader::Dashes);
paragraph->get_ParagraphFormat()->get_TabStops()->Add(tabStop);

// 2 -  Pass the values for properties of a new tab stop to the "Add" method:
paragraph->get_ParagraphFormat()->get_TabStops()->Add(ConvertUtil::MillimeterToPoint(100), TabAlignment::Left, TabLeader::Dashes);

// Add tab stops at 5 cm to all paragraphs.
for (const auto& para : System::IterateOver(doc->GetChildNodes(NodeType::Paragraph, true)->LINQ_OfType<SharedPtr<Paragraph>>()))
{
    para->get_ParagraphFormat()->get_TabStops()->Add(ConvertUtil::MillimeterToPoint(50), TabAlignment::Left, TabLeader::Dashes);
}

// Every "tab" character takes the builder's cursor to the location of the next tab stop.
auto builder = MakeObject<DocumentBuilder>(doc);
builder->Writeln(u"Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc->Save(ArtifactsDir + u"TabStopCollection.AddTabStops.docx");
```

## See Also

* Class [TabStop](../../tabstop/)
* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## TabStopCollection::Add(double, Aspose::Words::TabAlignment, Aspose::Words::TabLeader) method


Adds or replaces a tab stop in the collection.

```cpp
void Aspose::Words::TabStopCollection::Add(double position, Aspose::Words::TabAlignment alignment, Aspose::Words::TabLeader leader)
```


| Parameter | Type | Description |
| --- | --- | --- |
| position | double | A position (in points) where to add the tab stop. |
| alignment | Aspose::Words::TabAlignment | A [TabAlignment](../../tabalignment/) value that specifies the alignment of text at the tab stop. |
| leader | Aspose::Words::TabLeader | A [TabLeader](../../tableader/) value that specifies the type of the leader line displayed under the tab character. |
## Remarks


If a tab stop already exists at the specified position, it is replaced.

## Examples



Shows how to add custom tab stops to a document. 
```cpp
auto doc = MakeObject<Document>();
auto paragraph = System::ExplicitCast<Paragraph>(doc->GetChild(NodeType::Paragraph, 0, true));

// Below are two ways of adding tab stops to a paragraph's collection of tab stops via the "ParagraphFormat" property.
// 1 -  Create a "TabStop" object, and then add it to the collection:
auto tabStop = MakeObject<TabStop>(ConvertUtil::InchToPoint(3), TabAlignment::Left, TabLeader::Dashes);
paragraph->get_ParagraphFormat()->get_TabStops()->Add(tabStop);

// 2 -  Pass the values for properties of a new tab stop to the "Add" method:
paragraph->get_ParagraphFormat()->get_TabStops()->Add(ConvertUtil::MillimeterToPoint(100), TabAlignment::Left, TabLeader::Dashes);

// Add tab stops at 5 cm to all paragraphs.
for (const auto& para : System::IterateOver(doc->GetChildNodes(NodeType::Paragraph, true)->LINQ_OfType<SharedPtr<Paragraph>>()))
{
    para->get_ParagraphFormat()->get_TabStops()->Add(ConvertUtil::MillimeterToPoint(50), TabAlignment::Left, TabLeader::Dashes);
}

// Every "tab" character takes the builder's cursor to the location of the next tab stop.
auto builder = MakeObject<DocumentBuilder>(doc);
builder->Writeln(u"Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc->Save(ArtifactsDir + u"TabStopCollection.AddTabStops.docx");
```

## See Also

* Enum [TabAlignment](../../tabalignment/)
* Enum [TabLeader](../../tableader/)
* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
