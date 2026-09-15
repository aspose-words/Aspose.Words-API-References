---
title: "فئة Aspose::Words::Lists::ListFormat"
linktitle: "ListFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Lists::ListFormat. يسمح بالتحكم في تنسيق القائمة المطبق على الفقرة. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.lists/listformat/
---
## ListFormat class


يسمح بالتحكم في تنسيق القائمة المطبق على فقرة. لمعرفة المزيد، زر مقالة الوثائق [Working with Lists](https://docs.aspose.com/words/cpp/working-with-lists/).

```cpp
class ListFormat : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [ApplyBulletDefault](./applybulletdefault/)() | يبدأ قائمة نقطية افتراضية جديدة ويطبقها على الفقرة. |
| [ApplyNumberDefault](./applynumberdefault/)() | يبدأ قائمة مرقمة افتراضية جديدة ويطبقها على الفقرة. |
| [get_IsListItem](./get_islistitem/)() | صحيح عندما يكون للفقرة تنسيق نقطي أو مرقم مطبق عليها. |
| [get_List](./get_list/)() | يحصل أو يعيّن القائمة التي تكون هذه الفقرة عضوًا فيها. |
| [get_ListLevel](./get_listlevel/)() | يرجع تنسيق مستوى القائمة بالإضافة إلى أي تعديلات تنسيق مطبقة على الفقرة الحالية. |
| [get_ListLevelNumber](./get_listlevelnumber/)() | يحصل أو يعيّن رقم مستوى القائمة (من 0 إلى 8) للفقرة. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ListIndent](./listindent/)() | يزيد مستوى القائمة للفقرة الحالية بمستوى واحد. |
| [ListOutdent](./listoutdent/)() | يقلل مستوى القائمة للفقرة الحالية بمستوى واحد. |
| [RemoveNumbers](./removenumbers/)() | يزيل الأرقام أو النقاط من الفقرة الحالية ويضبط مستوى القائمة إلى الصفر. |
| [set_List](./set_list/)(const System::SharedPtr\<Aspose::Words::Lists::List\>\&) | معين لـ [Aspose::Words::Lists::ListFormat::get_List](./get_list/). |
| [set_ListLevelNumber](./set_listlevelnumber/)(int32_t) | معين لـ [Aspose::Words::Lists::ListFormat::get_ListLevelNumber](./get_listlevelnumber/). |
| static [Type](./type/)() |  |
## ملاحظات


يمكن أن تكون الفقرة في مستند Microsoft Word نقطية أو مرقمة. عندما تكون الفقرة نقطية أو مرقمة، يقال إن تنسيق القائمة تم تطبيقه على الفقرة.

لا تقوم بإنشاء كائنات من الفئة [ListFormat](./) مباشرة. يمكنك الوصول إلى [ListFormat](./) كخاصية لكائن آخر يمكن أن يكون له تنسيق قائمة مرتبط به. في الوقت الحالي، الكائنات التي يمكن أن يكون لها تنسيق قائمة هي: [Paragraph](../../aspose.words/paragraph/)، [Style](../../aspose.words/style/) و[DocumentBuilder](../../aspose.words/documentbuilder/).

[ListFormat](./) of a [Paragraph](../../aspose.words/paragraph/) specifies what list formatting and list level is applied to that particular paragraph.

[ListFormat](./) of a [Style](../../aspose.words/style/) (applicable to paragraph styles only) allows to specify what list formatting and list level is applied to all paragraphs of that particular style.

[ListFormat](./) of a [DocumentBuilder](../../aspose.words/documentbuilder/) provides access to the list formatting at the current cursor position inside the [DocumentBuilder](../../aspose.words/documentbuilder/).

يتم تخزين تنسيق القائمة نفسه داخل كائن [List](../list/) يتم تخزينه بشكل منفصل عن الفقرات. تُخزن كائنات القائمة داخل مجموعة [ListCollection](../listcollection/). هناك مجموعة [ListCollection](../listcollection/) واحدة لكل [Document](../../aspose.words/document/).

الفقرات لا تنتمي فعليًا إلى قائمة. الفقرات فقط تشير إلى كائن قائمة معين عبر الخاصية [List](./get_list/) ومستوى معين في القائمة عبر الخاصية [ListLevelNumber](./get_listlevelnumber/). من خلال تعيين هاتين الخاصيتين، تتحكم في ما يتم تطبيقه من نقاط وترقيم على الفقرة.

## أمثلة



يعرض كيفية العمل مع مستويات القوائم.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

// تتيح لنا القائمة تنظيم وتزيين مجموعات الفقرات باستخدام رموز البادئة والمسافات البادئة.
// يمكننا إنشاء قوائم متداخلة بزيادة مستوى المسافة البادئة.
// يمكننا بدء وإنهاء قائمة باستخدام خاصية "ListFormat" لكائن Document Builder.
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
// فيما يلي نوعان من القوائم يمكننا إنشاؤهما باستخدام Document Builder.
// 1 -  قائمة مرقمة:
// القوائم المرقمة تُنشئ ترتيبًا منطقيًا للفقرات عن طريق ترقيم كل عنصر.
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault));

ASSERT_TRUE(builder->get_ListFormat()->get_IsListItem());

// عن طريق ضبط الخاصية "ListLevelNumber"، يمكننا زيادة مستوى القائمة
// لبدء قائمة فرعية مستقلة عند عنصر القائمة الحالي.
// قالب القائمة في Microsoft Word المسمى "NumberDefault" يستخدم الأرقام لإنشاء مستويات القائمة للمستوى الأول.
// المستويات الأعمق للقائمة تستخدم الأحرف والأرقام الرومانية الصغيرة.
for (int32_t i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(System::String(u"Level ") + i);
}

// 2 -  قائمة نقطية:
// ستُطبق هذه القائمة مسافة بادئة ورمز نقطي ("•") قبل كل فقرة.
// المستويات الأعمق لهذه القائمة ستستخدم رموزًا مختلفة، مثل "■" و "○".
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));

for (int32_t i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(System::String(u"Level ") + i);
}

// يمكننا تعطيل تنسيق القوائم لتجنب تنسيق أي فقرات لاحقة كقوائم عن طريق إلغاء تعيين علامة "List".
builder->get_ListFormat()->set_List(nullptr);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

doc->Save(get_ArtifactsDir() + u"Lists.SpecifyListLevel.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
