---
title: "Aspose::Words::Style::get_UnhideWhenUsed yöntemi"
linktitle: "get_UnhideWhenUsed"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Style::get_UnhideWhenUsed yöntemi. Geçerli belgede kullanılan stilin Stiller galerisinden ve Stiller görev bölmesinden gizlenip gizlenmediğini alır/ayarlar. Kullanılan stil Stiller galerisinde gösterilmesi gerektiğinde C++'ta True olur."
type: docs
weight: 19500
url: /tr/cpp/aspose.words/style/get_unhidewhenused/
---
## Style::get_UnhideWhenUsed method


Geçerli belgede kullanılan stilin Styles galerisinden ve Styles görev bölmesinden gizlenip gizlenmediğini alır/ayarlar. Stil galerisinde gösterilmesi gerektiğinde doğru (true) olur.

```cpp
bool Aspose::Words::Style::get_UnhideWhenUsed() const
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
