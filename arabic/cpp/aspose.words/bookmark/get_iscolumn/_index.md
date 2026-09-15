---
title: "طريقة Aspose::Words::Bookmark::get_IsColumn"
linktitle: "get_IsColumn"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Bookmark::get_IsColumn. تُعيد true إذا كانت هذه العلامة المرجعية علامة مرجعية لعمود جدول في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words/bookmark/get_iscolumn/
---
## Bookmark::get_IsColumn method


يرجع **true** إذا كانت هذه الإشارة المرجعية إشارة عمود جدول.

```cpp
bool Aspose::Words::Bookmark::get_IsColumn()
```


## أمثلة



يوضح كيفية الحصول على معلومات حول إشارات مرجعية لأعمدة الجدول.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table column bookmarks.doc");

for (auto&& bookmark : System::IterateOver(doc->get_Range()->get_Bookmarks()))
{
    // إذا كانت الإشارة المرجعية تحيط بأعمدة جدول، فإنها تكون إشارة مرجعية لعمود جدول، ويتم تعيين علم IsColumn إلى true.
    std::cout << System::String::Format(u"Bookmark: {0}{1}", bookmark->get_Name(), (bookmark->get_IsColumn() ? System::String(u" (Column)") : System::String(u""))) << std::endl;
    if (bookmark->get_IsColumn())
    {
        auto row = System::AsCast<Aspose::Words::Tables::Row>(bookmark->get_BookmarkStart()->GetAncestor(Aspose::Words::NodeType::Row));
        if (row != nullptr && bookmark->get_FirstColumn() < row->get_Cells()->get_Count())
        {
            // اطبع محتويات العمودين الأول والأخير اللذين تحيط بهما الإشارة المرجعية.
            std::cout << row->get_Cells()->idx_get(bookmark->get_FirstColumn())->GetText().TrimEnd(System::MakeArray<char16_t>({Aspose::Words::ControlChar::CellChar})) << std::endl;
            std::cout << row->get_Cells()->idx_get(bookmark->get_LastColumn())->GetText().TrimEnd(System::MakeArray<char16_t>({Aspose::Words::ControlChar::CellChar})) << std::endl;
        }
    }
}
```

## انظر أيضًا

* Class [Bookmark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
