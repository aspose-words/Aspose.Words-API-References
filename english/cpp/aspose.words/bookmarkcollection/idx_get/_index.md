---
title: Aspose::Words::BookmarkCollection::idx_get method
linktitle: idx_get
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::BookmarkCollection::idx_get method. Returns a bookmark by name in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words/bookmarkcollection/idx_get/
---
## BookmarkCollection::idx_get(const System::String\&) method


Returns a bookmark by name.

```cpp
System::SharedPtr<Aspose::Words::Bookmark> Aspose::Words::BookmarkCollection::idx_get(const System::String &bookmarkName)
```


| Parameter | Type | Description |
| --- | --- | --- |
| bookmarkName | const System::String\& | Case-insensitive name of the bookmark. |
## Remarks


Returns **null** if the bookmark with the specified name cannot be found.

## See Also

* Class [Bookmark](../../bookmark/)
* Class [BookmarkCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## BookmarkCollection::idx_get(int32_t) method


Returns a bookmark at the specified index.

```cpp
System::SharedPtr<Aspose::Words::Bookmark> Aspose::Words::BookmarkCollection::idx_get(int32_t index)
```


| Parameter | Type | Description |
| --- | --- | --- |
| index | int32_t | An index into the collection. |
## Remarks


The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.

## See Also

* Class [Bookmark](../../bookmark/)
* Class [BookmarkCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
