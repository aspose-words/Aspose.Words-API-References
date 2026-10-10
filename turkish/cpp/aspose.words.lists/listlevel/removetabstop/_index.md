---
title: "Aspose::Words::Lists::ListLevel::RemoveTabStop metodu"
linktitle: "RemoveTabStop"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Lists::ListLevel::RemoveTabStop metodu. C++'de liste seviyesinden sekme durağını kaldırır."
type: docs
weight: 22500
url: /tr/cpp/aspose.words.lists/listlevel/removetabstop/
---
## ListLevel::RemoveTabStop method


Liste seviyesinden sekme durağını kaldırır.

```cpp
void Aspose::Words::Lists::ListLevel::RemoveTabStop()
```


## Örnekler



Liste seviyesi sekme durağını nasıl temizleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Varsayılan biçimlendirme ile bir liste oluşturun
builder->get_ListFormat()->ApplyNumberDefault();
builder->Writeln(u"Numbered list item 1");
builder->Writeln(u"Numbered list item 2");

// Liste seviyesini alın ve sekme durağını kaldırın
System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = builder->get_ListFormat()->get_ListLevel();
listLevel->RemoveTabStop();

doc->Save(get_ArtifactsDir() + u"Paragraph.RemoveTabStopFromListLevel.docx");
```

## Ayrıca Bakınız

* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
