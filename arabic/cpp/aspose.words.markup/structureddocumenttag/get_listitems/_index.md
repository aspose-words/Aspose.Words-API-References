---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_ListItems طريقة"
linktitle: "get_ListItems"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_ListItems طريقة. يحصل على SdtListItemCollection المرتبط بهذا الـ SDT في C++."
type: docs
weight: 21000
url: /ar/cpp/aspose.words.markup/structureddocumenttag/get_listitems/
---
## StructuredDocumentTag::get_ListItems method


يحصل على [SdtListItemCollection](../../sdtlistitemcollection/) المرتبط بهذا **SDT**.

```cpp
System::SharedPtr<Aspose::Words::Markup::SdtListItemCollection> Aspose::Words::Markup::StructuredDocumentTag::get_ListItems()
```

## ملاحظات


سيعمل الوصول إلى هذه الخاصية فقط مع أنواع SDT من [ComboBox](../../sdttype/) أو [DropDownList](../../sdttype/).

ستحدث استثناء لجميع أنواع SDT الأخرى.

## أمثلة



يوضح كيفية العمل مع علامات مستند منظم من نوع قائمة منسدلة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::DropDownList, Aspose::Words::Markup::MarkupLevel::Block);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(tag);

// علامة مستند منظم من نوع قائمة منسدلة هي نموذج يسمح للمستخدم بـ
// اختيار خيار من قائمة بالنقر بالزر الأيسر وفتح النموذج في Microsoft Word.
// خاصية "ListItems" تحتوي على جميع عناصر القائمة، وكل عنصر قائمة هو "SdtListItem".
System::SharedPtr<Aspose::Words::Markup::SdtListItemCollection> listItems = tag->get_ListItems();
listItems->Add(System::MakeObject<Aspose::Words::Markup::SdtListItem>(u"Value 1"));

ASSERT_EQ(listItems->idx_get(0)->get_DisplayText(), listItems->idx_get(0)->get_Value());

// أضف 3 عناصر قائمة أخرى. قم بتهيئة هذه العناصر باستخدام مُنشئ مختلف عن العنصر الأول
// لعرض سلاسل نصية مختلفة عن قيمها.
listItems->Add(System::MakeObject<Aspose::Words::Markup::SdtListItem>(u"Item 2", u"Value 2"));
listItems->Add(System::MakeObject<Aspose::Words::Markup::SdtListItem>(u"Item 3", u"Value 3"));
listItems->Add(System::MakeObject<Aspose::Words::Markup::SdtListItem>(u"Item 4", u"Value 4"));

ASSERT_EQ(4, listItems->get_Count());

// القائمة المنسدلة تعرض العنصر الأول. عيّن عنصر قائمة مختلف إلى "SelectedValue" لعرضه.
listItems->set_SelectedValue(listItems->idx_get(3));

ASSERT_EQ(u"Value 4", listItems->get_SelectedValue()->get_Value());

// قم بالتعداد عبر المجموعة واطبع كل عنصر.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::SdtListItem>>> enumerator = listItems->GetEnumerator();
    while (enumerator->MoveNext())
    {
        if (enumerator->get_Current() != nullptr)
        {
            std::cout << System::String::Format(u"List item: {0}, value: {1}", enumerator->get_Current()->get_DisplayText(), enumerator->get_Current()->get_Value()) << std::endl;
        }
    }
}

// احذف العنصر الأخير من القائمة.
listItems->RemoveAt(3);

ASSERT_EQ(3, listItems->get_Count());

// نظرًا لأن عنصر التحكم القائم على القائمة المنسدلة مضبوط لعرض العنصر المحذوف افتراضيًا، قدم له عنصرًا لعرضه موجودًا.
listItems->set_SelectedValue(listItems->idx_get(1));

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.ListItemCollection.docx");

// استخدم طريقة "Clear" لإفراغ مجموعة عناصر القائمة المنسدلة بالكامل مرة واحدة.
listItems->Clear();

ASSERT_EQ(0, listItems->get_Count());
```

## انظر أيضًا

* Class [SdtListItemCollection](../../sdtlistitemcollection/)
* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
