---
title: "Aspose::Words::Style::get_Priority metodu"
linktitle: "get_Priority"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Style::get_Priority metodu. Stilleri Styles görev bölmesinde sıralamak için önceliği temsil eden tam sayı değerini alır/ayarlar C++'ta."
type: docs
weight: 16334
url: /tr/cpp/aspose.words/style/get_priority/
---
## Style::get_Priority method


Stiller görev bölmesinde stilleri sıralama önceliğini temsil eden tam sayı değerini alır/ayar.

```cpp
int32_t Aspose::Words::Style::get_Priority() const
```


## Örnekler



Bir stilin önceliklendirilmesini ve gizlenmesini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Style> styleTitle = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Subtitle);

if (styleTitle->get_Priority() == 9)
{
    styleTitle->set_Priority(10);
}

if (!styleTitle->get_UnhideWhenUsed())
{
    styleTitle->set_UnhideWhenUsed(true);
}

if (styleTitle->get_SemiHidden())
{
    styleTitle->set_SemiHidden(true);
}

doc->Save(get_ArtifactsDir() + u"Styles.StylePriority.docx");
```

## Ayrıca Bakınız

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
