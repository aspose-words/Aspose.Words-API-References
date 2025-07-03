---
title: Aspose::Words::TabStopCollection::Before method
linktitle: Before
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::TabStopCollection::Before method. Gets a first tab stop to the left of the specified position in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words/tabstopcollection/before/
---
## TabStopCollection::Before method


Gets a first tab stop to the left of the specified position.

```cpp
System::SharedPtr<Aspose::Words::TabStop> Aspose::Words::TabStopCollection::Before(double position)
```


| Parameter | Type | Description |
| --- | --- | --- |
| position | double | The reference position (in points). |

### ReturnValue

A tab stop object or **null** if a suitable tab stop was not found.
## Remarks


Skips tab stops with [Alignment](../../tabstop/get_alignment/) set to [Bar](../../tabalignment/).

## Examples



Shows how to work with a document's collection of tab stops. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = builder->get_ParagraphFormat()->get_TabStops();

// 72 points is one "inch" on the Microsoft Word tab stop ruler.
tabStops->Add(System::MakeObject<Aspose::Words::TabStop>(72.0));
tabStops->Add(System::MakeObject<Aspose::Words::TabStop>(432.0, Aspose::Words::TabAlignment::Right, Aspose::Words::TabLeader::Dashes));

ASSERT_EQ(2, tabStops->get_Count());
ASSERT_FALSE(tabStops->idx_get(0)->get_IsClear());
ASSERT_FALSE(System::ObjectExt::Equals(tabStops->idx_get(0), tabStops->idx_get(1)));

// Every "tab" character takes the builder's cursor to the location of the next tab stop.
builder->Writeln(u"Start\tTab 1\tTab 2");

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(2, paragraphs->get_Count());

// Each paragraph gets its tab stop collection, which clones its values from the document builder's tab stop collection.
ASPOSE_ASSERT_EQ(paragraphs->idx_get(0)->get_ParagraphFormat()->get_TabStops(), paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops());
ASPOSE_ASSERT_NS(paragraphs->idx_get(0)->get_ParagraphFormat()->get_TabStops(), paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops());

// A tab stop collection can point us to TabStops before and after certain positions.
ASPOSE_ASSERT_EQ(72.0, tabStops->Before(100.0)->get_Position());
ASPOSE_ASSERT_EQ(432.0, tabStops->After(100.0)->get_Position());

// We can clear a paragraph's tab stop collection to revert to the default tabbing behavior.
paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops()->Clear();

ASSERT_EQ(0, paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops()->get_Count());

doc->Save(get_ArtifactsDir() + u"TabStopCollection.TabStopCollection.docx");
```

## See Also

* Class [TabStop](../../tabstop/)
* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
