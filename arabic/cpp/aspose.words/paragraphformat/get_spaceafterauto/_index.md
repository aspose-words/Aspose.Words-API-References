---
title: "طريقة Aspose::Words::ParagraphFormat::get_SpaceAfterAuto"
linktitle: "get_SpaceAfterAuto"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::ParagraphFormat::get_SpaceAfterAuto. صحيح إذا تم ضبط مقدار التباعد بعد الفقرة تلقائيًا في C++."
type: docs
weight: 32000
url: /ar/cpp/aspose.words/paragraphformat/get_spaceafterauto/
---
## ParagraphFormat::get_SpaceAfterAuto method


صحيح إذا تم تعيين مقدار المسافة بعد الفقرة تلقائيًا.

```cpp
bool Aspose::Words::ParagraphFormat::get_SpaceAfterAuto()
```

## ملاحظات


عند ضبطه إلى **true**, يتجاوز تأثير [SpaceAfter](../get_spaceafter/).

عند ضبطك مساحة الفقرة قبل وبعد إلى تلقائي، يضيف **Microsoft** Word تباعدًا قدره 14 نقطة بين الفقرات تلقائيًا وفقًا للقواعد التالية:

* Normally, spacing is added after all paragraphs.
* In a bulleted or numbered list, spacing is added only after the last item in the list. Spacing is not added between the list items.
* In a nested bulleted or numbered list spacing is not added.
* Spacing is normally added after a table.
* Spacing is not added after a table if it is the last block in a table cell.
* Spacing is not added after the last paragraph in a table cell.



## أمثلة



يظهر كيفية ضبط التباعد التلقائي للفقرات.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// تطبيق كمية كبيرة من المسافة قبل وبعد الفقرات التي سيُنشئها هذا المُنشئ.
builder->get_ParagraphFormat()->set_SpaceBefore(24);
builder->get_ParagraphFormat()->set_SpaceAfter(24);

// اضبط هذه العلامات إلى "true" لتطبيق التباعد التلقائي،
// مع تجاهل التباعد في الخصائص التي ضبطناها أعلاه بفعالية.
// تركها كـ "false" سيطبق التباعد المخصص للفقرات.
builder->get_ParagraphFormat()->set_SpaceAfterAuto(autoSpacing);
builder->get_ParagraphFormat()->set_SpaceBeforeAuto(autoSpacing);

// أدرج فقرتين سيكون لهما تباعد فوق وتحتهما واحفظ المستند.
builder->Writeln(u"Paragraph 1.");
builder->Writeln(u"Paragraph 2.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphSpacingAuto.docx");
```

## انظر أيضًا

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
