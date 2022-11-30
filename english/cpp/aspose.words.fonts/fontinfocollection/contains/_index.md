---
title: Contains
second_title: Aspose.Words for C++ API Reference
description: Determines whether the collection contains a font with the given name.
type: docs
weight: 40
url: /cpp/aspose.words.fonts/fontinfocollection/contains/
---
## FontInfoCollection::Contains method


Determines whether the collection contains a font with the given name.

```cpp
bool Aspose::Words::Fonts::FontInfoCollection::Contains(const System::String &name)
```


| Parameter | Type | Description |
| --- | --- | --- |
| name | const System::String\& | Case-insensitive name of the font to locate. |

### ReturnValue

True if the item is found in the collection; otherwise, false.

## Examples



Shows info about the fonts that are present in the blank document. 
```cpp
auto doc = MakeObject<Document>();

// A blank document contains 3 default fonts. Each font in the document
// will have a corresponding FontInfo object which contains details about that font.
ASSERT_EQ(3, doc->get_FontInfos()->get_Count());

ASSERT_TRUE(doc->get_FontInfos()->Contains(u"Times New Roman"));
ASSERT_EQ(204, doc->get_FontInfos()->idx_get(u"Times New Roman")->get_Charset());

ASSERT_TRUE(doc->get_FontInfos()->Contains(u"Symbol"));
ASSERT_TRUE(doc->get_FontInfos()->Contains(u"Arial"));
```

## See Also

* Class [FontInfoCollection](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words](../../../)
