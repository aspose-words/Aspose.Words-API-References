---
title: "Aspose::Words::TextColumnCollection فئة"
linktitle: "TextColumnCollection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::TextColumnCollection. مجموعة من كائنات TextColumn التي تمثل جميع أعمدة النص في قسم من المستند. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 71000
url: /ar/cpp/aspose.words/textcolumncollection/
---
## TextColumnCollection class


مجموعة من كائنات [TextColumn](../textcolumn/) التي تمثل جميع أعمدة النص في قسم من المستند. لمعرفة المزيد، زر مقالة الوثائق [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/).

```cpp
class TextColumnCollection : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_Count](./get_count/)() | يحصل على عدد الأعمدة في قسم المستند. |
| [get_EvenlySpaced](./get_evenlyspaced/)() | صحيح إذا كانت أعمدة النص ذات عرض متساوٍ وموزعة بالتساوي. |
| [get_LineBetween](./get_linebetween/)() | عند **true**، يضيف خطًا عموديًا بين الأعمدة. |
| [get_Spacing](./get_spacing/)() | عند توزيع الأعمدة بالتساوي، يحصل أو يحدد مقدار المسافة بين كل عمود بالنقاط. |
| [get_Width](./get_width/)() | عند توزيع الأعمدة بالتساوي، يحصل على عرض الأعمدة. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | يرجع عمود نص عند الفهرس المحدد. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_EvenlySpaced](./set_evenlyspaced/)(bool) | محدد لـ [Aspose::Words::TextColumnCollection::get_EvenlySpaced](./get_evenlyspaced/). |
| [set_LineBetween](./set_linebetween/)(bool) | محدد لـ [Aspose::Words::TextColumnCollection::get_LineBetween](./get_linebetween/). |
| [set_Spacing](./set_spacing/)(double) | محدد لـ [Aspose::Words::TextColumnCollection::get_Spacing](./get_spacing/). |
| [SetCount](./setcount/)(int32_t) | ينظم النص في عدد محدد من الأعمدة النصية. |
| static [Type](./type/)() |  |
## ملاحظات


استخدم [SetCount()](./setcount/) لتحديد عدد الأعمدة النصية.

لجعل جميع الأعمدة ذات عرض متساوٍ وموزعة بالتساوي، اضبط [EvenlySpaced](./get_evenlyspaced/) إلى **true** وحدد مقدار المسافة بين الأعمدة في [Spacing](./get_spacing/). سيقوم MS Word بحساب عرض الأعمدة تلقائيًا.

إذا كان لديك [EvenlySpaced](./get_evenlyspaced/) مضبوطًا على **false**، تحتاج إلى تحديد العرض والمسافة لكل عمود على حدة. استخدم الفهرس للوصول إلى كائنات [TextColumn](../textcolumn/) الفردية.

عند استخدام عروض أعمدة مخصصة، تأكد من أن مجموع جميع عروض الأعمدة والمسافات بينها يساوي عرض الصفحة مطروحًا منه هوامش الصفحة اليسرى واليمنى.

## أمثلة



يوضح كيفية إنشاء أعمدة متعددة موزعة بالتساوي في قسم.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::TextColumnCollection> columns = builder->get_PageSetup()->get_TextColumns();
columns->set_Spacing(100);
columns->SetCount(2);

builder->Writeln(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");

doc->Save(get_ArtifactsDir() + u"PageSetup.ColumnsSameWidth.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
