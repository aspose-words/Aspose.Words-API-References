---
title: "Aspose::Words::Font::get_StyleIdentifier طريقة"
linktitle: "get_StyleIdentifier"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Font::get_StyleIdentifier. يحصل على أو يضبط معرف النمط المستقل عن الإعدادات المحلية لنمط الأحرف المطبق على هذا التنسيق في C++."
type: docs
weight: 43000
url: /ar/cpp/aspose.words/font/get_styleidentifier/
---
## Font::get_StyleIdentifier method


الحصول أو تعيين معرف النمط المستقل عن اللغة لنمط الحرف المطبق على هذا التنسيق.

```cpp
Aspose::Words::StyleIdentifier Aspose::Words::Font::get_StyleIdentifier()
```


## أمثلة



يظهر كيفية تغيير نمط النص الموجود.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// فيما يلي طريقتان للإشارة إلى الأنماط.
// 1 -  استخدام اسم النمط:
builder->get_Font()->set_StyleName(u"Emphasis");
builder->Writeln(u"Text originally in \"Emphasis\" style");

// 2 -  استخدام معرف نمط مدمج:
builder->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::IntenseEmphasis);
builder->Writeln(u"Text originally in \"Intense Emphasis\" style");

// تحويل جميع استخدامات نمط واحد إلى آخر،
// باستخدام الطرق المذكورة أعلاه للإشارة إلى الأنماط القديمة والجديدة.
for (auto&& run : System::IterateOver<Aspose::Words::Run>(doc->GetChildNodes(Aspose::Words::NodeType::Run, true)))
{
    if (run->get_Font()->get_StyleName() == u"Emphasis")
    {
        run->get_Font()->set_StyleName(u"Strong");
    }

    if (run->get_Font()->get_StyleIdentifier() == Aspose::Words::StyleIdentifier::IntenseEmphasis)
    {
        run->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Strong);
    }
}

doc->Save(get_ArtifactsDir() + u"Font.ChangeStyle.docx");
```

## انظر أيضًا

* Enum [StyleIdentifier](../../styleidentifier/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
