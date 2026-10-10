---
title: "فئة Aspose::Words::Fonts::FontInfoCollection"
linktitle: "FontInfoCollection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Fonts::FontInfoCollection. تمثل مجموعة من الخطوط المستخدمة في مستند. لمعرفة المزيد، قم بزيارة مقالة الوثائق في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.fonts/fontinfocollection/
---
## FontInfoCollection class


يمثل مجموعة من الخطوط المستخدمة في مستند. لمعرفة المزيد، زر مقالة الوثائق [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FontInfoCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Fonts::FontInfo>>
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Contains](./contains/)(const System::String\&) | يحدد ما إذا كانت المجموعة تحتوي على خط بالاسم المحدد. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | يحصل على عدد العناصر الموجودة في المجموعة. |
| [get_EmbedSystemFonts](./get_embedsystemfonts/)() const | يحدد ما إذا كان سيتم تضمين خطوط النظام في المستند أم لا. القيمة الافتراضية لهذه الخاصية هي **false**. يعمل هذا الخيار فقط عندما يكون خيار [EmbedTrueTypeFonts](./get_embedtruetypefonts/) مضبوطًا على **true**. |
| [get_EmbedTrueTypeFonts](./get_embedtruetypefonts/)() const | يحدد ما إذا كان سيتم تضمين خطوط TrueType في المستند عند حفظه أم لا. القيمة الافتراضية لهذه الخاصية هي **false**. |
| [get_SaveSubsetFonts](./get_savesubsetfonts/)() const | يحدد ما إذا كان سيتم حفظ جزء من خطوط TrueType المضمنة مع المستند أم لا. القيمة الافتراضية لهذه الخاصية هي **false**. يعمل هذا الخيار فقط عندما تكون الخاصية [EmbedTrueTypeFonts](./get_embedtruetypefonts/) مضبوطة على **true**. |
| [GetEnumerator](./getenumerator/)() override | يرجع كائن عداد يمكن استخدامه للتنقل عبر جميع العناصر في المجموعة. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | يحصل على خط بالاسم المحدد. |
| [idx_get](./idx_get/)(int32_t) | يحصل على خط في الفهرس المحدد. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_EmbedSystemFonts](./set_embedsystemfonts/)(bool) | دالة تعيين للخاصية [Aspose::Words::Fonts::FontInfoCollection::get_EmbedSystemFonts](./get_embedsystemfonts/). |
| [set_EmbedTrueTypeFonts](./set_embedtruetypefonts/)(bool) | دالة تعيين للخاصية [Aspose::Words::Fonts::FontInfoCollection::get_EmbedTrueTypeFonts](./get_embedtruetypefonts/). |
| [set_SaveSubsetFonts](./set_savesubsetfonts/)(bool) | دالة تعيين للخاصية [Aspose::Words::Fonts::FontInfoCollection::get_SaveSubsetFonts](./get_savesubsetfonts/). |
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
## ملاحظات


العناصر هي كائنات [FontInfo](../fontinfo/).

لا تقوم بإنشاء مثيلات من هذه الفئة مباشرة. استخدم الخاصية [FontInfos](../../aspose.words/documentbase/get_fontinfos/) للوصول إلى مجموعة الخطوط المعرفة في المستند.

## أمثلة



يعرض كيفية طباعة تفاصيل الخطوط الموجودة في المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> allFonts = doc->get_FontInfos();

// اطبع جميع الخطوط المستخدمة وغير المستخدمة في المستند.
for (int32_t i = 0; i < allFonts->get_Count(); i++)
{
    std::cout << System::String::Format(u"Font index #{0}", i) << std::endl;
    std::cout << System::String::Format(u"\tName: {0}", allFonts->idx_get(i)->get_Name()) << std::endl;
    std::cout << System::String::Format(u"\tIs {0}a trueType font", (allFonts->idx_get(i)->get_IsTrueType() ? System::String(u"") : System::String(u"not "))) << std::endl;
}
```


يوضح كيفية حفظ مستند مع خطوط TrueType المضمنة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> fontInfos = doc->get_FontInfos();
fontInfos->set_EmbedTrueTypeFonts(embedAllFonts);
fontInfos->set_EmbedSystemFonts(embedAllFonts);
fontInfos->set_SaveSubsetFonts(embedAllFonts);

doc->Save(get_ArtifactsDir() + u"Font.FontInfoCollection.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
