---
title: "Aspose::Words::Style::get_SemiHidden metodu"
linktitle: "get_SemiHidden"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Style::get_SemiHidden metodu. Stil'in Styles galerisinden ve Styles görev bölmesinden gizlenip gizlenmediğini alır/ayarlar C++'ta."
type: docs
weight: 16667
url: /tr/cpp/aspose.words/style/get_semihidden/
---
## Style::get_SemiHidden method


Stilin Styles galerisinden ve Styles görev bölmesinden gizlenip gizlenmediğini alır/ayarlar.

```cpp
bool Aspose::Words::Style::get_SemiHidden() const
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
