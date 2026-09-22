---
title: "Aspose::Words::Markup::SdtListItemCollection class"
linktitle: "SdtListItemCollection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Markup::SdtListItemCollection class. يوفر الوصول إلى عناصر SdtListItem لعلامة مستند منسقة. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words.markup/sdtlistitemcollection/
---
## SdtListItemCollection class


يوفر الوصول إلى عناصر [SdtListItem](../sdtlistitem/) لعلامة مستند منسقة. لمعرفة المزيد، زر مقالة الوثائق [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class SdtListItemCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::SdtListItem>>
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Markup::SdtListItem\>\&) | يضيف عنصرًا إلى هذه المجموعة. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | يمسح جميع العناصر من هذه المجموعة. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | يحصل على عدد العناصر في المجموعة. |
| [get_SelectedValue](./get_selectedvalue/)() | يحدد القيمة المحددة حاليًا في هذه القائمة. يُسمح بالقيمة الفارغة، مما يعني عدم ارتباط أي إدخال محدد حاليًا بمجموعة عناصر هذه القائمة. |
| [GetEnumerator](./getenumerator/)() override | يرجع كائن عداد يمكن استخدامه للتنقل عبر جميع العناصر في المجموعة. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | يعيد كائن [SdtListItem](../sdtlistitem/) بناءً على فهرسه الصفري في المجموعة. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [RemoveAt](./removeat/)(int32_t) | يزيل عنصر قائمة في الفهرس المحدد. |
| [set_SelectedValue](./set_selectedvalue/)(const System::SharedPtr\<Aspose::Words::Markup::SdtListItem\>\&) | دالة ضبط لـ [Aspose::Words::Markup::SdtListItemCollection::get_SelectedValue](./get_selectedvalue/). |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| تعريف نوع | الوصف |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |

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

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
