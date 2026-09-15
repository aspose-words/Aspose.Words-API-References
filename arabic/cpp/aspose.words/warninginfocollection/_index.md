---
title: "فئة Aspose::Words::WarningInfoCollection"
linktitle: "WarningInfoCollection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::WarningInfoCollection. تمثل مجموعة مكتوبة من كائنات WarningInfo. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 75000
url: /ar/cpp/aspose.words/warninginfocollection/
---
## WarningInfoCollection class


تمثل مجموعة مكتوبة من كائنات [WarningInfo](../warninginfo/). لمعرفة المزيد، زر مقالة الوثائق [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class WarningInfoCollection : public Aspose::Words::IWarningCallback,
                              public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::WarningInfo>>
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | يزيل جميع العناصر من المجموعة. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | يحصل على عدد العناصر الموجودة في المجموعة. |
| [GetEnumerator](./getenumerator/)() override | يرجع كائن عداد يمكن استخدامه للتنقل عبر جميع العناصر في المجموعة. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | يحصل على عنصر في الفهرس المحدد. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
| [Warning](./warning/)(System::SharedPtr\<Aspose::Words::WarningInfo\>) override | ينفّذ واجهة [IWarningCallback](../iwarningcallback/). يضيف تحذيرًا إلى هذه المجموعة. |
| [WarningInfoCollection](./warninginfocollection/)() |  |
## Typedefs

| تعريف نوع | الوصف |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## ملاحظات


يمكنك استخدام كائن المجموعة هذا كأبسط شكل من تنفيذ [IWarningCallback](../iwarningcallback/) لجمع جميع التحذيرات التي يولدها Aspose.Words أثناء عملية التحميل أو الحفظ. أنشئ مثيلًا من هذه الفئة وعيّنها إلى خاصية [WarningCallback](../../aspose.words.loading/loadoptions/get_warningcallback/) أو [WarningCallback](../documentbase/get_warningcallback/).

## أمثلة



يظهر كيفية ضبط الخاصية للعثور على أقرب تطابق لخط مفقود من مصادر الخطوط المتاحة.
```cpp
// افتح مستندًا يحتوي على نص منسق بخط غير موجود في أي من مصادر الخطوط لدينا.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing font.docx");

// عيّن رد نداء لمعالجة تحذيرات استبدال الخطوط.
auto warningCollector = System::MakeObject<Aspose::Words::WarningInfoCollection>();
doc->set_WarningCallback(warningCollector);

// حدد اسم خط افتراضي وقم بتمكين استبدال الخط.
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Arial");
fontSettings->get_SubstitutionSettings()->get_FontInfoSubstitution()->set_Enabled(true);

// يجب استخدام مقاييس الخط الأصلي بعد استبدال الخط.
doc->get_LayoutOptions()->set_KeepOriginalFontMetrics(true);

// سوف نحصل على تحذير استبدال الخط إذا حفظنا مستندًا بخط مفقود.
doc->set_FontSettings(fontSettings);
doc->Save(get_ArtifactsDir() + u"FontSettings.EnableFontSubstitution.pdf");

for (auto&& info : warningCollector)
{
    if (info->get_WarningType() == Aspose::Words::WarningType::FontSubstitution)
    {
        std::cout << info->get_Description() << std::endl;
    }
}
```

## انظر أيضًا

* Interface [IWarningCallback](../iwarningcallback/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
