---
title: "Aspose::Words::TabStopCollection::Add method"
linktitle: "Add"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::TabStopCollection::Add metodu. C++'ta koleksiyonda bir sekme durağı ekler veya değiştirir."
type: docs
weight: 2000
url: /tr/cpp/aspose.words/tabstopcollection/add/
---
## TabStopCollection::Add(const System::SharedPtr\<Aspose::Words::TabStop\>\&) method


Koleksiyonda bir sekme durak noktasını ekler veya değiştirir.

```cpp
void Aspose::Words::TabStopCollection::Add(const System::SharedPtr<Aspose::Words::TabStop> &tabStop)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| tabStop | const System::SharedPtr\<Aspose::Words::TabStop\>\& | Eklenecek bir sekme durağı nesnesi. |
## Açıklamalar


Belirtilen konumda zaten bir sekme durağı varsa, değiştirilir.

## Örnekler



Özel sekme duraklarını bir belgeye nasıl ekleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto paragraph = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

// Aşağıda, "ParagraphFormat" özelliği aracılığıyla bir paragrafın sekme durakları koleksiyonuna sekme durakları eklemenin iki yolu verilmiştir.
// 1 -  Bir "TabStop" nesnesi oluşturun ve ardından koleksiyona ekleyin:
auto tabStop = System::MakeObject<Aspose::Words::TabStop>(Aspose::Words::ConvertUtil::InchToPoint(3), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
paragraph->get_ParagraphFormat()->get_TabStops()->Add(tabStop);

// 2 -  Yeni bir sekme durağının özellik değerlerini "Add" metoduna geçirin:
paragraph->get_ParagraphFormat()->get_TabStops()->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(100), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

// Tüm paragraflara 5 cm'de sekme durakları ekleyin.
for (auto&& para : System::IterateOver(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()))
{
    para->get_ParagraphFormat()->get_TabStops()->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(50), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
}

// Her "tab" karakteri, oluşturucunun imlecini bir sonraki sekme durak noktasının konumuna götürür.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc->Save(get_ArtifactsDir() + u"TabStopCollection.AddTabStops.docx");
```

## Ayrıca Bakınız

* Class [TabStop](../../tabstop/)
* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## TabStopCollection::Add(double, Aspose::Words::TabAlignment, Aspose::Words::TabLeader) method


Koleksiyonda bir sekme durak noktasını ekler veya değiştirir.

```cpp
void Aspose::Words::TabStopCollection::Add(double position, Aspose::Words::TabAlignment alignment, Aspose::Words::TabLeader leader)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| konum | double | Sekme durağının ekleneceği bir konum (puan cinsinden). |
| alignment | Aspose::Words::TabAlignment | Sekme durağındaki metnin hizalamasını belirten bir [TabAlignment](../../tabalignment/) değeri. |
| leader | Aspose::Words::TabLeader | Sekme karakterinin altında görüntülenen lider çizgi tipini belirten bir [TabLeader](../../tableader/) değeri. |
## Açıklamalar


Belirtilen konumda zaten bir sekme durağı varsa, değiştirilir.

## Örnekler



Özel sekme duraklarını bir belgeye nasıl ekleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto paragraph = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

// Aşağıda, "ParagraphFormat" özelliği aracılığıyla bir paragrafın sekme durakları koleksiyonuna sekme durakları eklemenin iki yolu verilmiştir.
// 1 -  Bir "TabStop" nesnesi oluşturun ve ardından koleksiyona ekleyin:
auto tabStop = System::MakeObject<Aspose::Words::TabStop>(Aspose::Words::ConvertUtil::InchToPoint(3), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
paragraph->get_ParagraphFormat()->get_TabStops()->Add(tabStop);

// 2 -  Yeni bir sekme durağının özellik değerlerini "Add" metoduna geçirin:
paragraph->get_ParagraphFormat()->get_TabStops()->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(100), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

// Tüm paragraflara 5 cm'de sekme durakları ekleyin.
for (auto&& para : System::IterateOver(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()))
{
    para->get_ParagraphFormat()->get_TabStops()->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(50), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
}

// Her "tab" karakteri, oluşturucunun imlecini bir sonraki sekme durak noktasının konumuna götürür.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc->Save(get_ArtifactsDir() + u"TabStopCollection.AddTabStops.docx");
```

## Ayrıca Bakınız

* Enum [TabAlignment](../../tabalignment/)
* Enum [TabLeader](../../tableader/)
* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
