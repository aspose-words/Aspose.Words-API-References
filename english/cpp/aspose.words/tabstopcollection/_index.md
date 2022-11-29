---
title: TabStopCollection
second_title: Aspose.Words for C++ API Reference
description: A collection of TabStop objects that represent custom tabs for a paragraph or a style.
type: docs
weight: 885
url: /cpp/aspose.words/tabstopcollection/
---
## TabStopCollection class


A collection of [TabStop](../tabstop/) objects that represent custom tabs for a paragraph or a style.

```cpp
class TabStopCollection : public Aspose::Words::InternableComplexAttr,
                          public Aspose::Words::IExpandableAttr
```

## Methods

| Method | Description |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::TabStop\>\&) | Adds or replaces a tab stop in the collection. |
| [Add](./add/)(double, Aspose::Words::TabAlignment, Aspose::Words::TabLeader) | Adds or replaces a tab stop in the collection. |
| [After](./after/)(double) | Gets a first tab stop to the right of the specified position. |
| [Before](./before/)(double) | Gets a first tab stop to the left of the specified position. |
| [Clear](./clear/)() | Deletes all tab stop positions. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::TabStopCollection\>\&) | Determines whether the specified [TabStopCollection](./) is equal in value to the current [TabStopCollection](./). |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Determines whether the specified object is equal in value to the current object. |
| [get_Count](./get_count/)() | Gets the number of tab stops in the collection. |
| [GetHashCode](./gethashcode/)() const override | Serves as a hash function for this type. |
| [GetIndexByPosition](./getindexbyposition/)(double) | Gets the index of a tab stop with the specified position in points. |
| [GetPositionByIndex](./getpositionbyindex/)(int32_t) | Gets the position (in points) of the tab stop at the specified index. |
| [idx_get](./idx_get/)(int32_t) | Gets a tab stop at the given index. |
| [idx_get](./idx_get/)(double) | Gets a tab stop at the specified position. |
| [RemoveByIndex](./removebyindex/)(int32_t) | Removes a tab stop at the specified index from the collection. |
| [RemoveByPosition](./removebyposition/)(double) | Removes a tab stop at the specified position from the collection. |
## Remarks


In Microsoft Word documents, a tab stop can be defined in the properties of a paragraph style or directly in the properties of a paragraph. A style can be based on another style. Therefore, the complete set of tab stops for a given object is a combination of tab stops defined directly on this object and tab stops inherited from the parent styles.

In Aspose.Words, when you obtain a **TabStops** collection for a paragraph or a style, it contains only the custom tab stops defined directly for this paragraph or style. The collection does not include tab stops defined in the parent styles or default tab stops.

## Examples



Shows how to work with a document's collection of tab stops. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<TabStopCollection> tabStops = builder->get_ParagraphFormat()->get_TabStops();

// 72 points is one "inch" on the Microsoft Word tab stop ruler.
tabStops->Add(MakeObject<TabStop>(72.0));
tabStops->Add(MakeObject<TabStop>(432.0, TabAlignment::Right, TabLeader::Dashes));

ASSERT_EQ(2, tabStops->get_Count());
ASSERT_FALSE(tabStops->idx_get(0)->get_IsClear());
ASSERT_FALSE(System::ObjectExt::Equals(tabStops->idx_get(0), tabStops->idx_get(1)));

// Every "tab" character takes the builder's cursor to the location of the next tab stop.
builder->Writeln(u"Start\tTab 1\tTab 2");

SharedPtr<ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

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

doc->Save(ArtifactsDir + u"TabStopCollection.TabStopCollection.docx");
```

## See Also

* Class [InternableComplexAttr](../internablecomplexattr/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words](../../)
